**WDI Fundamentals Unit 3**

---

##![Your Turn](../assets/exercise.png) Your Turn


If you haven't already, fork and clone the [wdi-fundamentals-exercises]() repo to your desktop; then, go into the `lib` directory and open up the file called `some_expressions.js`.

Inside this file, you should see the following text:

```javascript

function someNumber() {
  return /*Your Expression*/;
}

function someString() {
  return /*Your Expression*/;
}

function someBoolean() {
  return /*Your Expression*/;
}

```

`/*Your Expression*/`, above, is called a *comment* - it tells the computer to completely ignore everything between the two `/` characters. There are two kinds of comments: 'span'/'multi-line' comments (`/* comment */`), which can run across multiple lines, and 'single-line' comments (`// comment`), which can't.

Your job, in this exercise, is to replace each of those comments with an expression - any expression you like - that evaluates to either `360`, `"Hello world"`, or `true`, respectively.

Once you've finished writing, save `some_expressions.js`, copy the entire contents of the file into repl.it's editor, and click the `>` button; there, you can check your answers in the console by entering the commands `someNumber()`, `someString()`, or `someBoolean()`.

If all three of those commands give you the correct answers, nice job - you're done! Now it's time to save those changes to our repository.

1. In your terminal, navigate to the `wdi-fundamentals-exercises` directory (you can check if you're there by typing `pwd`).
2. Check the status of the repo by typing `git status` - it should tell us that there are unsaved changes.
3. Type `git add lib/some_expressions.js`, which tells git to add this file to the next commit we make.
4. Finally type `git commit -m "Completes some_expressions.js"` to commit our changes to the repository, labelling these changes as "Completes some_expressions.js". Generally speaking, your commit messages should describe how the changes that you've made affect the repository as a whole.

[On to the next lesson.](04_lesson.md)
