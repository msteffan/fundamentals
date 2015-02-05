**WDI Fundamentals Unit 4**

---

## Your Turn

Here's the [starter code](http://repl.it/aAQ) for your next exercise:

```javascript
var x /* Test values of x here */;
var result;

if (x%3 === 0 && x%5 === 0) {
  result = 'fizzbuzz';
  } else if (x%3 === 0) {
  result = 'fizz';
  } else if (x%5 === 0) {
  result = 'buzz';
  } else {
  result = x;
}

var max;

/* WRITE YOUR CODE HERE */
```

Last time, we wrote code that took an input `x` and set a new `result` value according to a specific set of rules.

This time, your challenge is to loop through every number from 1 to `max`, applying the same rules to each number and, finally, printing the result to the console using the command `console.log(result);`.

For example, if you ran the finished code with `max` equal to 10, the following should be displayed in the console:

```javascript
  1
  2
  fizz
  4
  buzz
  fizz
  7
  8
  fizz
  buzz
```

---
Got it working? Nice job! [Let's review what we've covered this chapter.](08_cheatsheet.md)
