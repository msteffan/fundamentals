**WDI Fundamentals Unit 3**

---

## Project

Now that we've learned a little bit about expressions, let's apply some of this material to our 'Rock Paper Scissors' project.

- - -

Go back into the project repo, wherever you've decided to put it, and open up the file `RockPaperScissors.js` (inside the `app/js` directory).

When you look inside the file you should first see a block of code that looks like this :

```javascript
function getInput() {
    console.log("Please choose either 'rock', 'paper', or 'scissors'.")
    return prompt();
}
function randomPlay() {
    var randomNumber = Math.random();
    if (randomNumber < 0.33) {
        return "rock";
    } else if (randomNumber < 0.66) {
        return "paper";
    } else {
        return "scissors";
    }
}
```

Please don't edit this code, but feel free to look at it closely and try to figure out how it works - learning to read code is an important step in learning how to write code.

When you're ready, skip ahead to the next section, shown below.

```javascript
function getPlayerMove(move) {
    // Write an expression that operates on a variable called `move`
    // If a `move` has a value, your expression should evaluate to that value.
    // However, if `move` is not specified / is null, your expression should equal `getInput()`.
    return /* Your Expression */;
}

function getComputerMove(move) {
    // Write an expression that operates on a variable called `move`
    // If a `move` has a value, your expression should evaluate to that value.
    // However, if `move` is not specified / is null, your expression should equal `randomPlay()`.
    return /* Your Expression */;
}
```

Similar to how you've done this in your exercises, you will need to replace the `/* Your Expression */` comment with an expression of your own creation. Instructions for how this expression should behave are laid out in the single-line comments above.

> **CAUTION** For now, don't worry about what `getInput()` or `randomPlay()` are, and just ignore that `function somethingSomething()` stuff - we'll be covering all of that in depth in Chapter 5. Just focus on subbing in your new expressions.

Go ahead and get started - once you've finished editing those two lines, save your code and make a commit to the project's repository.

---
[Next up: Chapter 4](../04_chapter/README.md)
