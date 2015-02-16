**WDI Fundamentals Unit 5**

---

#Functional JavaScript

Functions can also be used as procedures - miniature, self-contained programs that are executed one line at a time whenever the function is called.

When you have a set of tasks that need to be repeated, it can often be helpful to turn that set of tasks into a function, and call it every time that the procedure should be run.

For instance, let's go back to the "French Toast a la GA" recipe from Unit 4.  
Every time a soaked slice of bread is ready to be cooked, we need to:


> 5: Transfer the slices to your frying pan and cook on a medium-low heat until brown on the bottom.
>

Rather than writing out explicitly how this should be done each time, we could write a function, (say `cookSoggyBread()`) to handle this set of instruuctions for us, and simply call that function any time the bread slices need to be cooked.

## Problem Solving with Functions

Let's look at a practical example. Say that we're working on a [TicTacToe game](http://en.wikipedia.org/wiki/Tic-tac-toe).

We're not going to build the actual game, just write out the logic that would determine the winner.

In TicTacToe, there are nine possible values (for every cell on the board):

```
| a | b | c |
| d | e | f |
| g | h | i |
```   

Each of these values will start as `null`, until a user assigns them a new value, either `'o'` or `'x'`

To play around with this invisible TicTacToe board, we've provided some code:

```javascript
function cellValue(key) {
    switch(key) {
        case 'a': return null;
        case 'b': return null;
        case 'c': return null;
        case 'd': return null;
        case 'e': return null;
        case 'f': return null;
        case 'g': return null;
        case 'h': return null;
        case 'i': return null;
        default : return null;
    }
}
```
To assign a value (`x`, `o`)to any cell on the board, edit the return value for the corresponding case.  For example, if you want the board to read:

```
    | null | null |   x  |
    | null |   o  | null |
    | null |   o  |   x  |
```    

You would edit the switch statement like such:

```javascript
function cellValue(key) {
    switch(key) {
        case 'a': return null;
        case 'b': return null;
        case 'c': return 'x';
        case 'd': return null;
        case 'e': return 'o';
        case 'f': return null;
        case 'g': return null;
        case 'h': return 'o';
        case 'i': return 'x';
        default : return null;
    }
}
```

###Who is the Winnner?

Now, let's write a function that determines the winner based on the values of a, b, c, d, e, f, g, h, and i.

We'll call it `getWinner` and it will give us back either `'x'` (if X has won), `'o'` (if O has won), or `null` (if neither side has won).

```javascript
  function getWinner() {
  }
```

So where do we go from here?

One way to determine the winner might be to check whether X has won and then to check whether O has won.What if two functions existed that would magically determine this for us? 

We could call them `winnerIsX` and `winnerIsO` - `winnerIsX` could give us back `true` if X has won and `false` if it hasn't. If such functions existed, we could rewrite `getWinner` like this:

```javascript
  function getWinner() {
    if (winnerIsX()) {
      return 'x';
    }
    if (winnerIsO()) {
      return 'o';
    }
    return null;
  }
```

OK! Now we're getting somewhere. Instead of solving one big problem, we're solving two smaller problems –how do we determine whether X or O won?

###Determing if `x` has won

Let's focus on `winnerIsX` first. 

In TicTacToe, there are three ways that X can win:
1. All cells in a row contain an `x`
2. All cells in a column contain an `x`
3. All cells in a diagonal contain an `x` 

Wouldn't it be great if we had functions to determine these too? We could call them `winsRowX`, `winsColumnX`, and `winsDiagonalX`. 

In this case, X would win if there were a row victory OR a column victory OR a diagonal victory, so to determine `winnerIsX` we could write the following:

```javascript
  function winnerIsX() {
    return winsRowX() || winsColumnX() || winsDiagonalX();
  }
```

You can't execute anything yet.  Just stick with us –we only have a few more tiny problems to solve!

####Winning by Rows

Let's look at `winsRowX` - what does it actually mean to win a row? 

According to our cell key from earlier, there are three cells in a row; the first row is `a`,`b`, and `c`; the second row is `d`,`e`, and `f`; the third row is `g`,`h`, and `i`.

If any of these three sets are all equal to `x`, then X has won via a row. 

Let's dive just one level deeper, with a function to test if any one of the three rows are equal to `x` (let's call it `allThreeX`).

```javascript
  function winsRowX() {
    return allThreeX(cellValue('a'), cellValue('b'), cellValue('c')) ||
    		allThreeX(cellValue('d'), cellValue('e'), cellValue('f')) ||
    		allThreeX(cellValue('g'), cellValue('h'), cellValue('i'));
  }
  function allThreeX(cell_one, cell_two, cell_three) {
  }
```

####Winning by Columns and Diagonals


We can also use `allThreeX` to write functions for `winsColumnX` and `winsDiagonalX`. This would give us the following code:

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

Now that we've broken it into one much smaller problem, our `allThreeX` function is fairly easy to write!

```javascript
  function allThreeX(cell_one, cell_two, cell_three) {
    return (cell_one === 'x') && (cell_two === 'x') && (cell_three === 'x');
  }
```

Excellent! Now, `isWinnerX` should be able to tell us if X has won.

###Determining if `o` has won

Now, we could go ahead and start writing a function called `allThreeO` to do the same thing for O as we've done for X. 

But that pretty duplicative - those functions would be exactly the same, except for that hard-coded value of 'x'. It would be better if we could make allThreeX more general. What if we rewrote it like this?

```javascript
  function allThree(player, cell_one, cell_two, cell_three) {
    return (cell_one === player) && (cell_two === player) && (cell_three === player);
  }
```

###Removing the duplicative code

Now `allThree` can be used to test for `x` **or** for `o`; by getting rid of our hard-coded data, we were able to make this function do double-duty!

Let's do the same thing for all the other functions we wrote:

```javascript
  function getWinner() {
    if (winnerIs('x')) {
      return 'x';
    }
    if (winnerIs('o')) {
      return 'o';
    }
    return null;
  }
  function winnerIs(player) {
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

If you want, you can play around with this code in [this repl.it session](http://repl.it/aOU), which also contains some dummy code to mock up how `cells` might work. Try testing each of the different functions with different input values, and see what happens.

Have fun!


---
[Here comes another quiz - do your best!](06_quiz.md)
