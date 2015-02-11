**WDI Fundamentals Unit 6**

---

##Your Turn

Here's a link to a repl.it session with the following [sample code](http://repl.it/abi) :
```javascript
  var checkerboard = [[null,null,null,null,null,null,null,null],
                      [null,null,null,null,null,null,null,null],
                      [null,null,null,null,null,null,null,null],
                      [null,null,null,null,null,null,null,null],
                      [null,null,null,null,null,null,null,null],
                      [null,null,null,null,null,null,null,null],
                      [null,null,null,null,null,null,null,null],
                      [null,null,null,null,null,null,null,null]];
  function setSquare(player, row, col) {
    // Your Code Here
  }

  function getPieceAt(row, col) {
    // Your Code Here
  }
  function clearBoard() {
    // Your Code Here
  }
```

In this exercise, we'll be laying the groundwork for a Checkers game. Your task is to implement two functions:
* `setSquare`, which places a player (either 'R' or 'B') at a particular row and column on the board.
* `getPieceAt`, which returns the piece at a particular row and column; if there's no piece at that position, it should return `null`.

As a challenge, see if you can successfully implement an additional function:
* `clearBoard`, which resets the entire board to null.

---
[Ready to move on? Here's the next lesson.](05_lesson.md)
