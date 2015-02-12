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
      var team = ['ted','lem','phil','linda','veronica',];
      team[team.length - 1]   // evaluates to 'veronica'.
      team[team.length - 2]   // evaluates to 'linda'.
    ```

* `.push(...)` and `.pop(...)`
  `push` and `pop` are two related functions that allow you to either add an element to (`push`) or remove the last element from (`pop`) the end of an array. `push` in particular a very convenient way to build up an array over time - you're simply adding another item to the list. As a side note (since it's rare to use them this way),`push` evaluates to the value of the element it's adding, while `pop` evaluates to the the value of the element it's just removed.
    ```javascript
      var ghosts = ['blinky','inky','pinky'];
      ghosts.push('clyde')  // evaluates to 'clyde'; `ghosts` is now ['blinky','inky','pinky','clyde'].
      ghosts.pop()          // evaluates to 'clyde'; `ghosts` is now ['blinky','inky','pinky'] again.
    ```

* `.indexOf(...)`
  This function evaluates to the index of the first element in the array that matches the value in parentheses. If no match is found, the function evaluates to -1.
    ```javascript
      var animals = ['bear','beetle','boa'];
      animals.indexOf('boa')  // evaluates to 2
      animals.indexOf('bear') // evaluates to 0
      animals.indexOf('bee')  // evaluates to -1
    ```

### Test Yourself
What will the following lines do? Check your answers in repl.it.
* `['a','b','c'].indexOf('b')`
* `[true,false,false,true].length`
* `x = ['paul','john','george']; x.push('ringo');`
* `y = ['soda','tart','weasel']; y.pop();`

> **NOTE** If you're interested in looking at more of the different functions that arrays can use on themselves, you might want to take a look at (and bookmark) [this page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) from the Mozilla Developer Network's JavaScript documentation. Try playing around with some of them on your own in repl.it!

---
[Test your understanding with this next quiz!](06_quiz.md)
