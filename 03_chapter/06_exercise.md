**WDI Fundamentals Unit 3**

---

##![Your Turn](../assets/exercise.png) Your Turn
<br>


You should already have the [wdi-fundamentals-exercises](./ch3-exercises) repo set up from the previous exercise. Go into that repo, and open up a file in the `lib` directory called `some_more_expressions.js`.

Inside this file, you should see the following text:

```javascript

function addTen(x) {
  // If x is 10, your expression should evaluate to 20.
  // If x is 50, your expression should evaluate to 60.
  return /*Your Expression*/;
}

function triplePlusFive(x) {
  // If x is 5, your expression should evaluate to 20.
  // If x is 20, your expression should evaluate to 65.
  return /*Your Expression*/;
}

function sayHello(name) {
  // If name is "Alice", your expression should evaluate to "Hello, Alice."
  // If name is "Bob", your expression should evaluate to "Hello, Bob."
  return /*Your Expression*/;
}

function sayGoodbye(name) {
  // If name is "Charlene", your expression should evaluate to "Goodbye, Charlene."
  // If name is "David", your expression should evaluate to "Goodbye, David."
  return /*Your Expression*/;
}

```

As in the previous exercise, your job is to replace each of those `/*Your Expression*/` comments with an expression. This time, however, the expression will need to depend on a variable. Take a look at one of those lines that says `function`; unlike last time, there should be a variable listed in the parentheses to the right. This variable represents an `input` that our expression will be using. Write your expressions so that they behave like the descriptions given in the single-line comments.

Once you've finished, save `some_more_expressions.js`, copy the entire contents of the file into repl.it's editor, and click the `>` button. Like last time, we'll be entering some commands (`addTen()`, `triplePlusFive()`,`sayHello()`, `sayGoodbye()`) into the console; however, this time, we'll need to specify some input values in order to see if our expressions were correct. We do this by putting input values in between the parentheses. For example, `addTen(5)` will use `5` as an input value; `sayHello("Max")` will use `"Max"` as an input value.

Try testing out all of the different 'test cases' specified in the file. If they all give you the answers that you expect, you're done! Go ahead and save those changes to our repository.

> In case you forgot, here's the process of how we commit our changes.
> 1. In your terminal, navigate to the `wdi-fundamentals-exercises` directory (you can check if you're there by typing `pwd`).
> 2. Check the status of the repo by typing `git status` - it should tell us that there are unsaved changes.
> 3. Type `git add lib/some_more_expressions.js`, which tells git to add this file to the next commit we make.
> 4. Finally type `git commit -m "Completes some_more_expressions.js"` to commit our changes to the repository, labelling these changes as "Completes some_more_expressions.js". Generally speaking, your commit messages should describe how the changes that you've made affect the repository as a whole.

[Next Lesson](06_lesson.md)
