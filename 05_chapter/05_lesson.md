**WDI Fundamentals Unit 5**

---

#Writing Your Own Functions

Suppose that we wanted to create a function called `sumOfCubes`, which would take four inputs (`a`,`b`,`c`, and `d`) and evaluate to `a` cubed plus `b` cubed plus `c` cubed plus `d` cubed. 

We could write that whole thing out explicitly, like so:

```javascript
  function sumOfCubes(a,b,c,d) {
    return (a * a * a) + (b * b * b) + (c * c * c) + (d * d * d);
  }
```

This function has a couple of practical issues.
* The `return` statement is very long and difficult to read; it'd be very easy to miss a typo.
* If we wanted to change the way we cube each paramater, we'd have to go back and change the cubing operation for each variable by hand. That's a lot of work, and presents another opportunity to make a mistake.

To fix these issues, let's break the function into two smaller ones:

```javascript
  function cubeOf(x) {
    return x * x * x;
  }
  function sumOfCubes(a,b,c,d) {
    return cubeOf(a) + cubeOf(b) + cubeOf(c) + cubeOf(d);
  }
```

See how much easier this is to read? You can tell how it's supposed to work at a glance - very helpful if someone else is looking at your code (which is almost always the case).

> **NOTE** Although there are many different perspectives about how to write good fuctions, here are a few basic guidelines:
  * **Keep your functions small and simple.** Don't try to do too much in a single step.
  * **Call things what they are.** A big part of what makes the code in our example readable is our choice of function names - they explicitly and succinctly refer to the value that's being returned (or, alternatively, the operation that is being done.)
  * **Avoid repetition where possible.** Though it's important not to get carried away with this, having less duplication in your code usually makes your code easier to read and simpler to maintain.
  * **Try to avoid hard-coding values inside your functions.** This typically makes your code more abstract and generalizable, allowing it to be reused in different contexts.

## Problem Solving with Functions
Let's look at a practical example. Say that we're working on a TicTacToe game. Fortunately, we're not the only ones on this project - our coworkers down the hall have taken care of getting input from the user. According to their notes, all nine cells' values will be accessible via a function called `cells`, which takes a string (e.g. 'a') as an input and evaluates to the value for that specific cell (as labelled below).

    | a | b | c |
    | d | e | f |
    | g | h | i |

Each cell's value will either be `'x'`, `'o'`, or `null`.

Our job is to write the game logic - specifically, the logic that detemines who, if anyone, has won the game. To do this, we'll be writing a function called `getWinner`; it should give us back either `'x'` (if X has won), `'o'` (if O has won), or `null` (if neither side has won).
```javascript
  function getWinner() {
  }
```
But where do we go from here?

One way to determine the winner might be to check if either X or O has won, or if neither has won. What if we had functions that could tell us those things? We could call them `isWinnerX` and `isWinnerO` - `isWinnerX` could give us back `true` if X has won and `false` if it hasn't. If such functions existed, we could rewrite `getWinner` like this:
```javascript
  function getWinner() {
    if (isWinnerX()) {
      return 'x';
    }
    if (isWinnerO()) {
      return 'o';
    }
    return null;
  }
```
OK! Now we're getting somewhere. Instead of solving one big problem, we're solving two smaller problems.

Let's focus on `isWinnerX` first - the solution to `isWinnerO` will probably be almost exactly the same. In TicTacToe, there are three ways that X can win: on a row, on a column, or on a diagonal. Wouldn't it be great if there were functions to determine those things? We could call them `winsRowX`, `winsColumnX`, and `winsDiagonalX`. In this case, X would win if there were a row victory OR a column victory OR a diagonal victory, so we write the following:
```javascript
  function getWinner() {
    if (isWinnerX()) {
      return 'x';
    }
    if (isWinnerO()) {
      return 'o';
    }
    return null;
  function isWinnerX() {
    return winsRowX() || winsColumnX() || winsDiagonalX();
  }
```
Even smaller problems!

Let's look at `winsRowX` - what does it mean to win a row? According to our table from earlier, there are three cells in a row; the first row is `a`,`b`, and `c`; the second row is `d`,`e`, and `f`; the third row is `g`,`h`, and `i`. It seems like if any of these three sets are all equal to `x`, then X has won via a row. Let's dive just one level deeper, with a function to test if any three variables are equal to `x` (let's call it `allThreeX`).
```javascript
  function winsRowX() {
    return allThreeX(cells('a'), cells('b'), cells('c')) ||
           allThreeX(cells('d'), cells('e'), cells('f')) ||
           allThreeX(cells('g'), cells('h'), cells('i'));
  }
  function allThreeX(cell_one, cell_two, cell_three) {
  }
```

We can also use `allThreeX` to write functions for `winsColumnX` and `winsDiagonalX`. This would give us the following code.

```javascript
  function getWinner() {
    if (isWinnerX()) {
      return 'x';
    }
    if (isWinnerO()) {
      return 'o';
    }
    return null;
  }
  function isWinnerX() {
    return winsRowX() || winsColumnX() || winsDiagonalX();
  }
  function winsRowX() {
    return allThreeX(cells('a'), cells('b'), cells('c')) ||
           allThreeX(cells('d'), cells('e'), cells('f')) ||
           allThreeX(cells('g'), cells('h'), cells('i'));
  }
  function winsColumnX() {
    return allThreeX(cells('a'), cells('d'), cells('g')) ||
           allThreeX(cells('b'), cells('e'), cells('h')) ||
           allThreeX(cells('c'), cells('f'), cells('i'));
  }
  function winsDiagonalX() {
    return allThreeX(cells('a'), cells('e'), cells('i')) || allThreeX(cells('c'), cells('e'), cells('g'));
  }
  function allThreeX(cell_one, cell_two, cell_three) {
  }
```

Now that we've broken it into a much smaller problem, our `allThreeX` function is fairly easy to write!
```javascript
  function allThreeX(cell_one, cell_two, cell_three) {
    return (cell_one === 'x') && (cell_two === 'x') && (cell_three === 'x');
  }
```

Excellent! Now, `isWinnerX` should be able to tell us if X has won.

Now, we could go ahead and start writing a function called `allThreeO` to do the same thing for O as we've done for X. But that pretty duplicative - those functions would be exactly the same, except for that hard-coded value of 'x'. It would be better if we could make allThreeX more general. What if we rewrote it like this?
```javascript
  function allThree(player, cell_one, cell_two, cell_three) {
    return (cell_one === player) && (cell_two === player) && (cell_three === player);
  }
```
Now `allThree` can be used to test for X **or** for O; by getting rid of our hard-coded data, we were able to make this function do double-duty!

Let's do the same thing for all the other functions we wrote.

```javascript
  function getWinner() {
    if (isWinner('x')) {
      return 'x';
    }
    if (isWinner('o')) {
      return 'o';
    }
    return null;
  }
  function isWinner(player) {
    return winsRow(player) || winsColumn(player) || winsDiagonal(player);
  }
  function winsRow(player) {
    return allThree(player, cells('a'), cells('b'), cells('c')) ||
           allThree(player, cells('d'), cells('e'), cells('f')) ||
           allThree(player, cells('g'), cells('h'), cells('i'));
  }
  function winsColumn(player) {
    return allThree(player, cells('a'), cells('d'), cells('g')) ||
           allThree(player, cells('b'), cells('e'), cells('h')) ||
           allThree(player, cells('c'), cells('f'), cells('i'));
  }
  function winsDiagonal(player) {
    return allThree(player, cells('a'), cells('e'), cells('i')) ||
           allThree(player, cells('c'), cells('e'), cells('g'));
  }
  function allThree(player, cell_one, cell_two, cell_three) {
    return (cell_one === player) && (cell_two === player) && (cell_three === player);
  }
```

If you want, you can play around with this code in [this repl.it session](http://repl.it/aOU), which also contains some dummy code to mock up how `cells` might work. Try testing each of the different functions with different input values, and see what happens!


---
[Here comes another quiz - do your best!](06_quiz.md)
