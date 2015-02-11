**WDI Fundamentals Unit 5**

---

# Other Important Things About Functions
As you probably realize, there'a a lot more to functions than what we've shown you so far. You should be able to figure out most of it by reading through documentation and experimenting on your own, but there are still a couple of topics that merit some deeper discussion.

## Anonymous Functions

As you may remember from the first lesson, when calling a function, it's necessary to include parentheses after the function's name. If you don't, instead of actually executing the function, you get back the function itself.
```javascript
  function myFunc() {
    ...
  }
```
```javascript
  myFunc

  => [Function]
```
> **NOTE** This is the response you'd get from repl.it. However, other consoles can behave a little differently - for instance, doing this in the Chrome Console (part of Chrome's Developer Tools) will actually show you the content of the function, not just `[Function]`.

What is actually going on here? Well, in JavaScript, any code we write (including functions) is just data - data that can be stored in a variable, and retrieved by calling that variable's name. In fact, JavaScript allows us to explicitly store functions inside variables, like so:
```javascript
  var someVar = function someFunction(x) {
    return x + 1;
  }
```
The function `someFunction` has been stored inside the variable `someVar` - we can retrive `someFunction` by evaluating `someVar` in the console.
```javascript
  someVar;

  => [Function : someFunction]
```
If we put parentheses after `someVar`, it will actually call `someFunction`, giving back the result of 25 (as specified in `someFunction`'s definition).
```javascript
  someVar(1)

  => 2
```
Neat! But what's especially interesting about this whole mechanic is that the name of the function (`someFunction`) is totally irrelevant - calling `someVar` would work exactly the same way if we named that function `banana`, `hedgehog`, or even - amazingly - nothing at all!
```javascript
  var someVar = function (x) {
    return x + 1;
  }
```
See how there's no function name specified above? This is what's known as an **anonymous function**. Ordinarily, since an anonymous function has no name, it's impossible to call it elsewhere in your program - just like any other value that isn't stored in a variable (for instance, the line `3;`), there's no way to refer to it. **HOWEVER**, because in this case our anonymous function has been stored inside the variable `someVar`, we *can* call it, by calling `someVar`. In effect, `someVar` has given our anonymous function a name that we can call! This is an extremely common practice in JavaScript, so much so that it is accepted as [one of the standard ways to define a function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions#Function_constructor_vs._function_declaration_vs._function_expression).

OK, that's kind of neat. But do we really need another way to define functions? Well, as it happens, there's another important use case for anonymous functions: *being used as inputs to other functions*. Sounds crazy? Well, take at look at the following.
```javascript
  function printFuncResults(some_func) {
    for (var i = 0; i < 10; i += 1) {
      console.log(some_func(i));
    }
    return null;
  }
```
`printFuncResults` is a function that accepts another function as an input, applying that function to every number between 0 and 9, and printing out the result each time. Although we could name a function elsewhere, and pass it in as an argument, it's unlikely that we'd need to use this function anywhere else. So why waste memory storing it indefinitely? It'd be much more efficient to simply create this function on the fly when we need it, and get rid of it when we're done.
```javascript
  printFuncResults(function(x) {return 2*x;})

    0
    2
    4
    6
    8
    10
    12
    14
    16
    18
  => null
```
As you can see, when `printFuncResults` was called, we passed in an anonymous function as an argument. Then, this function was applied to each number from 0 to 9, and the result was printed out in the terminal.

>**NOTE** This is a very common programming pattern - applying a specific function to every element in a set. We'll look a little more at how this can be implemented in Chapter 6.

You might be wondering: What's with all this 'reachable' stuff? Can't any function be used anywhere in a program? In fact, the answer is ***no*** (and it's a good thing, too). The specific rules of what parts of a program are accessible to what are set by something called **scoping**, and that's the last topic that we'll be looking at in this unit.

## Function Scope
Imagine that if every variable created inside our program was accessible everywhere. What would happen if we wanted to create two distinct variables, both called `number`? If we tried, the computer would have no way to distinguish between the two. We'd have to create separate variables, like `number`, `other_number`, `yet_another_number` etc. just to keep everything straight, and keeping track of all those different variations would be a hassle. Plus, any time we write a new variable, we've have to look through *every variable that exists* in order to make sure that there wasn't duplication. Worst of all, if we messed up, we might actually mess up how one function works by accidentally changing a key value from another function!

This kind of scheme, where variables are accessible everywhere, is called using **globally-scoped** (or **global**, for short) variables. As you can see, it leads to a lot of issues. In general, we want to avoid using global variables in our programs, for the reasons listed above. They have their time and place, but should be used *sparingly*.

The alternative to having a variable be globally-scoped is having it be **locally-scoped** / **local**. A local variable is created for, and destroyed after, the execution of the function that contains it. Function parameters are and example of local variables - if you try to access them from *outside* the function, you won't be able to.
```javascript
  function myFunc(x) {
    return x+1;
  }

  console.log(x); // Will give us the error `ReferenceError: x is not defined.`
```
We've actually been using local variables for a while - any variable that's defined with the keyword `var` is created as a local variable, existing only inside the function that contains it. Defining a variable *without* using `var` indicates (at least in JavaScript) that a variable is global.

>**NOTE** If you have a global variable and a local variable with the same name (say, `x`), the function containing the local variable will interpret `x` as the local variable, and act accordingly. However, even though this technically does not cause an error, it's generally a bad idea to use the same names for your global and local variables. (This is most easily accomplished by avoiding global variables in the first place).

What if we have a function defined within another function, like the example below? Where are those variables accessible?
```javascript
  var a = 0;
  function firstFunction() {
    var b = 1;

    function secondFunction() {
      var c = 2;

      var thirdFunction = function () {
        var d = 3;
      }

    }

  }
```
JavaScript uses a rule called **lexical scoping** to manage situations like this. This rules says that each function contains its own unique local scope, and any variables created there exist only within that scope; however, those variables are *also* accessible inside any functions that are defined within that scope.

```javascript
  // Outermost scope.
  var a = 0;

  function firstFunction() {
    // firstFunction's local scope
    var b = 1;

    function secondFunction() {
      // secondFunction's local scope
      var c = 2;

      var thirdFunction = function () {
        // thirdFunction's local scope
        var d = 3;
      }

    }

  }
```
<sup float="right">[1]</sup>

In the example above, `a`,`b`,`c`, and `d` are all accessible from `thirdFunction`'s local scope. However,
* `d` is not accessible from `secondFunction`'s local scope
* `c` and `d` are not accessible from `firstFunction`'s local scope
* `b`, `c`, and `d` are not accessible from the outermost local scope.

>**NOTE** In a way, local variables created in your program's outermost scope can almost be thought of as 'pseudo-global', since they can be accessed from anywhere in your program; the biggest difference between this and true global variables is that global variables can be defined anywhere in the program, not just in the outermost scope. However, doing this is **dangerous**, because it makes it hard to keep track of what global variables you have; it's one of the reasons why global variables are usually avoided. If you must use global variables, only define them in the outermost scope.

### Test Yourself
```javascript
  var x = 25;
  function funcOne() {
    var color = "green";
    function funcTwo() {
      var someNum = 1;
      function doAThing(){
        ...
      }
    }
    function funcThree(name) {
      var y = 9;
      var myFunc = function(alpha) {
        ...
      }
    }
  }
```
* Which variables are accessible inside `doAThing`?
* Which are accessible inside `funcThree`?
* What is accessible to something inside `myFunc`?

---
Ready for another quiz? [Let's go!](09_quiz.md)

<br>
<br>
<br>

<span lineheight="10px">[1] This exercise borrows conceptually from a [blog post](http://toddmotto.com/everything-you-wanted-to-know-about-javascript-scope/) by Todd Motto, lead front-end dev for a web consultancy called 'AppsBroker' - it does a good job of explaining how scope works in JavaScript, and also dives into other related topics like closures and context (not covered here). Feel free to give it a read-through!</span>
