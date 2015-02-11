**WDI Fundamentals Unit 6**

---

# Additional Array Features

In addition to containing multiple elements, arrays also have a number of in-built properties and functions that give it many useful abilities. Here are a couple of them:

  * `.length`
    All arrays have a property called `length`, which evaluates to the tell you how many elements are currently present in the array. To access this value, simply tack on `.length` to the end of an array (or, alternatively, a variable containing that array). Here are some examples of `.length` in action.
    ```javascript
      ['a','b','c'].length;
        // Evaluates to 3

      var x = [10,20,30,40];
      x.length;
        // Evaluates to 4
    ```

    One especially nice thing about knowing the length of the array is that it allows us to easily find the last (or second-to-last, or third-to-last) element in the array.
    ```javascript
      var my_array = ['ted','lem','phil','linda','veronica',];
      my_array[my_array.length - 1];
        // Evaluates to 'veronica'.
    ```

  * `.push(...)` and `.pop(...)`

  * `.shift(...)` and `.unshift(...)`

  * ``

### Test Yourself
*
*
*

> **NOTE** If you're interested in looking at more of the different functions that arrays can use on themselves, you might want to take a look at (and bookmark) [this page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) from the Mozilla Developer Network's JavaScript documentation. Try playing around with some of them on your own in repl.it!

---
[]()
