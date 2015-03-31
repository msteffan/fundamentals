**WDI Fundamentals Unit 6**

---

# Iterating Over Arrays

In the past few units, we've only been able to operate on one value at a time. One of the most useful things about a collection (and arrays in particular) is that, if we structure our code correctly, we can actually perform the same operation on *each value within a collection*. This process is called **iteration** - doing something over and over and over again, for each element in a set.

##Iterating with Loops

Suppose that we were given an array of starting values to work with - say, temperatures in degrees Fahrenheit - and wanted to convert them into another set of values - say temperatures in degrees Celsius - which would then be stored in a separate array.

```javascript
var tempsInF = [100, 72, 88, 15, 25, 32];
var tempsInC = [];
```

The formula for converting between Fahrenheit and Celsius temperatures is **C = (5 / 9 * F)  - 32**, where `F` is the temperature in degrees Fahrenheit and `C` is the temperature in degrees Celsius. Because this is an operation that we'd like to do frequently, we might create a function for it like the one below.

```javascript
function fahrToCelc(degrees) {
  return degrees * 5 / 9  - 32;
}
```
So how do we go about operating on the elements in `tempsInF`? Well, we could just start at the beginning and work our way through, one value at a time.
```javascript
tempsInC.push(fahrToCelc(tempsInF[0]));
```

Then, we could run an almost identical command to operate on each element in `tempsInF` and push the converted value onto the `tempsInC` array.

```javascript
  tempsInC.push(fahrToCelc(tempsInF[1]));
  tempsInC.push(fahrToCelc(tempsInF[2]));
  tempsInC.push(fahrToCelc(tempsInF[3]));
  tempsInC.push(fahrToCelc(tempsInF[4]));
  tempsInC.push(fahrToCelc(tempsInF[5]));
```

However, this code is extremely repetitious, and it also forces us to hard-code exactly how many times we want the operation to be performed. It'd be better if there were a way to run this code exactly as many times as there are elements in the first array. Fortunately, there is a tool perfectly suited for this task - our old friend the `for` loop.

```javascript
for (var i = 0; i < tempsInF.length; i += 1) {
  tempsInC.push(fahrToCelc(tempsInF[i]));
}
```

Take a minute to think about what's going on above.

By starting our count at zero, stopping before `i` reaches the length of the array, and increasing `i` by one every time, `i` will be successively set to the index of every element in our array, allowing us to perform the same operation on each element.

We could just as easily have gone in the opposite direction - starting at the last element, and ending with the first - simply by specifying different settings in the `for` loop:

```javascript
for (var i = (tempsInF.length - 1); i >= 0; i -= 1) {
  tempsInC.push(fahrToCelc(tempsInF[i]));
}
```

We could even operate only on every third element, by changing the value we increment i, like so (see `i += 3` ?):

```javascript
  for (var i = 2; i < tempsInF.length; i += 3) {
    tempsInC.push(fahrToCelc(tempsInF[i]));
  }
```

Despite being one of the most basic ways to iterate through an array, in JavaScript (and many other languages) this is also one of the most versatile ones!

### Test Yourself

Create a new repl.it session with the following JavaScript code:

```javascript
var oldArray = [12, 45, 6, 23, 19, 20, 20, 15, 30, 42];
```

How could you use iteration to generate a new array called `newArray` from `oldArray`, so that...
* Each value in `newArray` is the value of its corresponding element in `oldArray`, plus 5? (`[1, 2, 3]` becomes `[6, 7, 8]`)
* Each value in `newArray` is the square of the value of its corresponding element in `oldArray`? (`[1, 2, 3]` becomes `[1, 4, 9]`)
* Every *odd-indexed* value in `newArray` is double its corresponding element in `oldArray`, while every *even-indexed* value is unchanged? (`[3, 4, 5, 2, 6]` becomes `[3, 8, 5, 4, 6]`)
* `newArray` is the exact mirror image of `oldArray`? (`[1, 2, 3]` becomes `[3, 2, 1]`)

These ones are a bit tricky, so don't get discouraged if the answers don't come immediately; just keep experimenting with your code until it works!

## Iterator Functions : `.map()` and `.forEach()`

Although using loops to iterate through arrays gives you a lot of flexibility and control, most of the time you just want to go through every element in your array one at a time, in order, and doing this with a loop can be a little tedious. Fortunately, arrays have some built-functions specifically designed for this kind of work, called (unsurprisingly) **iterators**.

One of the most commonly used iterators is `.map()` - this is the tool of choice any time you want to transform one set of values into a different (but equally-dimensioned) set of values. Although it can take more paramaters, `.map()` can be run with just one : a function. Take a look at the example below:

```javascript
function square(x) {
  console.log(x * x);
  return x * x;
}

var resultingArray = [1, 2, 3].map(square); // prints out 1, 4, and 9, then returns the array [1, 4, 9] and stores it in resultingArray
```

>**WARNING** It's important that you *do not* include parentheses when passing in that function. Including `square` as an argument passes the whole function. Including `square()` as the argument would pass in the result of calling the function. That's not what you want, normally.

As you can see, `.map()` takes in the function we've just defined, `square`, as a parameter. It then applies that function to every element in our original array, and stores the result at that same position in a new array. Finally, the function returns the new array that it's just created. As you can see, this is both simpler and cleaner than trying to do the same thing with a loop.

Another example of an iterator is `.forEach()`. `.forEach()` also takes a function as an argument, but unlike `.map()`, it doesn't create a new array and return it. However, it does still execute the function that gets passed for each element in the array.

```javascript
function square(x) {
  console.log(x * x);
  return x * x;
}

var resultingArray = [1, 2, 3].forEach(square); // prints out 1, 4, and 9, but doesn't return an array. This means resultingArray is undefined :(
```

###Test Yourself

Try to implement each of the following things in repl.it using `.map()` and `.forEach()`
* Start with a variable `x` and an array of your choosing. Write an expression that will increase `x` by 10 once for every element in the array.
* Create an array of masses in kilograms, and use it to produce an array of those same masses in pounds (hint: it's roughly 2.2 pounds to the kilogram).
* Believe it or not, Strings have a `.length` property just like arrays do. Armed with this knowledge, create an array of strings, and use an iterator to produce an array containing the length of each string.

If you're interested, you can read the full documentation on `.map()` and `.forEach()` here:
* [.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
* [.forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

---
Feeling confident? [Test your understanding of iteration with this next quiz.](06_quiz.md)
