**WDI Fundamentals Unit 6**

---

##![Your Turn](../assets/exercise.png) Your Turn

In this exercise, we'll return to our checkers game one last time. This time, however, we won't be writing a function; instead, your mission, should you choose to accept it, is to create a nested array called `pieces` to store the locations of every piece on the board.

`pieces` should be an associative array, with two keys : 'red' and 'black'. Each of these keys should correspond to a normal array listing out all of the different pieces for that color. Each piece should be represented as a two-element array in the pattern of `[row,col]`; for example, the list of red pieces would include `[0,0]`, `[0,2]`, `[0,4]`, etc.

Here's that diagram again, in case you forgot how to set up the baord.

![Picture of Checkerboard](http://www.maniacworld.com/Checkers/checkers.jpg)

To test your work, run each of the following two operations in the repli.it console

```javascript
  pieces['red'].map(function(piece){
      var row = piece[0];
      var col = piece[1];
      return checkerboard[row][col] === 'R';
    });

  pieces['black'].map(function(piece){
      var row = piece[0];
      var col = piece[1];
      return checkerboard[row][col] === 'B';
    });
```

Each of these operations should return an array full of boolean values. If both arrays' values are all `true`, then congratulations - you're done!

---

Feeling confident? [Test your understanding of iteration with this next quiz.](09_quiz.md)
