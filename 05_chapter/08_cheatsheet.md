**WDI Fundamentals Unit 5**

---

# Functions Cheat Sheet

Here are some notes on what's been covered in this chapter; feel free to copy this and extend it to make your own cheatsheet.

## Functions

### Defining and Using JavaScript Functions

* A **function** is a custom operation that can be run on command. It can be use both as an operator (accepting input values and calculating output values) and as a subroutine (do this thing... then do this thing...).
* Functions must be **defined** before they can be used. To define a function, use the following recipe:

```javascript
function myFunctionName() {
  // Body of the function
}
```

* To use, or **call** a function, simply type the name of your function, followed by `()` (plus any inputs that you might be passing in).

```javascript
myFunctionName()
```


### `return` Statements
* In addition to specifying a final value for the function to give back as a result, a `return` statement will cause the function that contains it to immediately end when that line is run. For example, if the function below is operating on a number greater than ten, it will stop executing at its second line, and return 15, not `x`.

```javascript
function someFunc(x) {
  if (x > 10) {
    return 15;
  }
  return x;
}
```

## Using Functions in the Field

### Best Practices for Writing Functions
* In addition to functionality, making your code readable is one of the most critical things to consider.
* Here are some guidelines that you can keep in mind:
  * Keep you functions small - don't try to do too much in one step.
  * Use good naming for functions and variables. Call things what they are!
  * Avoid repetitive code, where possible.
  * Generally, don't hard-code specific values into your program if you can help it.


### Problem Solving with Functions
* Sometimes, when you're trying to figure out how to break apart a problem, it can be helpful to imagine functions that could accomplish specific pieces of it.
* Learning how to break down a complicated problem into smaller pieces is one of the most important parts of programming, and the best way to get better at it is to practice! In programming, we call this [decomposition](http://en.wikipedia.org/wiki/Decomposition_%28computer_science%29).


---
[Let's apply what we've learned about Functions to our 'Rock, Paper, Scissors' project.](09_assessment.md)
