**WDI Fundamentals Unit 3**

---

##![Your Turn](../assets/exercise.png) Your Turn

Follow [this link](http://repl.it/9gI) to some sample code in a repl.it session - it should contain the following code:

```javascript
console.log("Please Enter a Number");
//this console.log is here because this repl.it console does not display the prompt message, though any other environment would
var x = prompt("Please Enter a Number");
  // If x is 10, your expression should evaluate to 20.
  // If x is 50, your expression should evaluate to 60.
console.log(/* Your Expression */);

console.log("Please Enter a Number");
var y = prompt("Please Enter a Number");
  // If y is 5, your expression should evaluate to 20.
  // If y is 20, your expression should evaluate to 65.
console.log(/* Your Expression */);

console.log("What is your name?");
var name = prompt("What is your name?");
  // If name is "Alice", your expression should evaluate to "Hello, Alice."
  // If name is "Bob", your expression should evaluate to "Hello, Bob."
console.log(/* Your Expression */);

console.log("What is your name?");
var name = prompt("What is your name?");
  // If name is "Charlene", your expression should evaluate to "Goodbye, Charlene."
  // If name is "David", your expression should evaluate to "Goodbye, David."
console.log(/* Your Expression */);
```

As in the previous exercise, your job is to replace each of those `/*Your Expression*/` comments with an expression. 

This time, however, the expression will need to depend on a variable and this variable's value will be determined by a user input. There are several ways to get a value from a user in JavaScript, the simplest of which is to use `prompt`. It works by asking a user for an answer before they can continue and then assigning whatever they write to the variable you specify (in this case, `name`):

```javascript
var name = prompt("What is your name?");
console.log("Hello " + name);
```

While `prompt` expects a user to write something in repl.it, repl.it does not show the prompt message.  We've corrected that by writing the message to the console.

Write your expressions so that they behave like the descriptions given in the single-line comments. Test if your expressions work correctly by running the code in the console.

When you run your code, you should see the prompt message (visible because of the console.log line we added before we define the variable).

Write your input and hit <kbd>ENTER</kbd>.

Try testing out all of the different 'test cases' that the comments specify in the console. If they all give you the answers that you expect, you're done!

---
[Next : Expression Oddballs](08_lesson.md)
