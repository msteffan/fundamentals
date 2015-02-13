**WDI Fundamentals Unit 4**

---

## Project

Now that we've learned a bit more about how Functions work in JavaScript, let's revisit our 'Rock Paper Scissors' project.

---


Go back to `RockPaperScissors.js`, and scroll down to the following code:

```javascript
  function playToFive() {
    console.log("Let's play Rock Paper Scissors");
    var playerWins = 0;
    var computerWins = 0;
    // This function should continue to play Rock Paper Scissors until either the player or the computer has won five times.
    // After each 'round', display some text in the console indicating who played what, who won, and what the current scoreboard looks like.
    // For example,
    //  console.log("Player chose " + playerMove + " while Computer chose " + computerMove);
    //  console.log("The score is currently " + playerWins + " to " + computerWins + "\n");

    /* YOUR CODE HERE */

    return [playerWins, computerWins];
}
```

As you might infer from the title, the purpose of this function is to run the 'Rock Paper Scissors' game until either the player or the computer has won a total of five games. 

Please write whatever code will be necessary for this function to work.

Once your code is working, you can commit your changes and move on to the next chapter.

[Next up: Chapter 6](../06_chapter/README.md)

> If any of you are interested in an additional challenge, try writing another function called `playTo(x)` that allows us to play Rock Paper Scissors until either the player or the computer has won `x` times. Feel free to steal liberally from `playToFive()`.