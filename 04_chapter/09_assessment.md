**WDI Fundamentals Unit 4**

---

## Project

Let's use what we've just learned about control flow to make some more progress on our 'Rock Paper Scissors' project.

---

Open up `RockPaperScissors.js` in your text editor of choice, and scroll down to the following code:

```javascript
function getWinner(playerMove,computerMove) {
    // This function should either give us back 'player', 'computer', or 'tie'.
    // The rules of the game are that rock beats scissors, scissors beats paper, and paper beats rock.
    // Assume that the only possible input values we can get are 'rock', 'paper', and 'scissors'.
}
```

Use control flow to determine which value gets `return`ed.
> HINT: the possible outcomes are either 'player' (if the player wins), 'computer' (if the computer wins), or 'tie' (if it's a draw).

If you're still feeling stuck, take a look back at [Chapter 3](../03_chapter/README.md). What expression could we write to tell us if the player (or computer) has won? What expression could tell us if there was a tie?

> **Note** Remember, when you're programming, you need to figure out the solution before you ever start writing code. Here's a good general procedure you can follow:
>
> 1. **Understand the problem.** In particular, try to determine (a) what you will be given, and (b) what you hope to get out. If you can't explain the problem in those kinds of terms, you won't be able to move further.
>
> 2. **Come up with test cases (and eventually, tests).** Once you've figured out how your code is supposed to behave generally, pick out a couple of specific cases that you can use to confirm whether or not your code is working. Once you've learned a little more about writing code, you'll actually use these test cases to write tester code, which can be used to automatically confirm whether or not your project's code is working.
>> Actually, this project has some tests built into it already, using a testing tool called Jasmine; to see the tests up close, just take a peek inside (but don't change!) the file `RockPaperScissorsSpec.js`, which sits inside the `spec` directory. These tests specify exactly how the code we write should behave - that's why they're called 'specs'!
>
> 3. **Solve the problem in English.** Or any human language, really. The point is, it's a good idea to pause and avoid *touching* your keyboard until you can start to explain, clearly and precisely, both what it is you're trying to do and how you're trying to do it. You can try sketching out the concept or outlining your procedure on paper, if it helps.
>
> 4. **Write code, even if it's not the prettiest.** Don't worry at this stage if your code is elegant, readable, or robust. Just make it work enough to satisfy all of your test cases.
>
> 5. **'Refactor' your code.** Now that everything works, take come time to make your code clean/efficient/robust/whatever in addition to functional. Just make sure that whatever changes you make don't break your code - you can keep an eye on this by testing your code and making sure that it still gives you the correct results.

Once you've finished (and have tested your code), commit the changes you've made to the project's repository.

---
[Next up: Chapter 5](../05_chapter/README.md)
