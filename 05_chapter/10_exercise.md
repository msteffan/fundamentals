**WDI Fundamentals Unit 5**

---

##![Your Turn](../assets/exercise.png) Your Turn

Building off of the `printFuncResults` example in the lesson, in this exercise we'll be writing a function called `applyTwice`. There's no starter code this time, so go ahead an open a fresh session in repl.it

`applyTwice` takes two parameters : `x`, an integer, and `some_function`, an anonymous function. `applyTwice` will work by applying the anonymous function to `x` twice, like so:
```javascript
  applyTwice(10, function(num) {return 2*num;})

  => 40
```

Test your code using any number `x` you choose, passing in the following anonymous functions as inputs. Did you get the answers you expected?
```javascript
  function (num) {return num + 1;}
  function (num) {return num * num;}
  function (num) {return -1 * num;}
  function (val) {return !val;}    // You can use a boolean value for `x` with this example, but you don't have to - remember, non-boolean values are still truthy/falsey.
```

Now write three of your own anonymous functions and try passing them into `applyTwice`. When you've got all three working, you're done!

---
[Let's review everything we've covered in this unit.](11_cheatsheet.md)
