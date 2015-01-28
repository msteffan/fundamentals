**WDI Fundamentals Unit 4 - Flow Control**

---

## Your Turn

Follow [this link]() to another repl.it session - it should contain the following code:

```javascript
  function fizzOrBuzz(x) {
    if (x%3 == 0 && x%5 == 0) {
      return 'fizzbuzz';
    } else if (x%3 == 0) {
      return 'fizz';
    } else if (x%5 == 0) {
      return 'buzz'
    } else {
      return x;
    }
  }

  function fizzbuzz(num) {
    // YOUR CODE HERE
  }
```

Replace that comment with code that will print out the result of `fizzOrBuzz()` to the console (using the command `console.log();`) for every number from 1 to `x`.

To test your code, run `fizzbuzz(20)` in the console; you should get back the result

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
 11
 fizz
 13
 14
 fizzbuzz
 16
 17
 fizz
 19
 buzz
```

---
[Let's review.](08_cheatsheet.md)
