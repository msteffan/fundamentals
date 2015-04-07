**WDI Fundamentals Unit 6**

---

As of the last time you worked on `wdi-fundamentals-rps`, you should have the following working functions:
  * `getPlayerMove` which (unless a move is provided as a parameter) prompts the user for input
  * `getComputerMove` which (unless a move is provided as a parameter) generates a random move for the computer
  * `getWinner` which takes two parameters (representing the player's and computer's moves, respectively) and evaluates to either 'player', 'computer', or 'tie' based on the moves that the player and computer are making.
  * `playToFive` which runs the Rock Paper Scissors game until either the player or the computer has won five times.

Now it's time to submit the project.

## Merging with Upstream

Before we do anything else, we should make sure that our project is still in sync with the original repo. Run the following commands in the terminal:

```bash
git remote add upstream https://github.com/ga-students/wdi-fundamentals-rps.git
```

Here, we add another remote (link to a repo) to our local copy of the repository. If you type `git remote -v` you should now see an `origin` remote pointing to your forked copy of the repo, and an `upstream` remote pointing to the original one.

Next, we want to make sure that if anyone modified the "upstream" or original repo, we have all those changes incorporated into our local one. To do that, type:

```bash
git pull upstream student
```

> **WARNING** Since these commands tell Git to try to merge the latest version of the original repository with the version you have on your computer, you could run into some conflicts between your files and the files on the remote. You probably won't hit any issues here, but it's possible that you might get a scary-looking error message. Post to the #wdi-fundamentals channel if that's the case, and we'll make sure you get help.

At this point, if all goes well, you'll be asked to make another commit. Enter your commit message in the following format (replace the date with the start date of your course) so that we can identify your work when we look through all of the submissions.

 `"WDI Boston 2010-01-01 :: John Doe"`

## Making a Pull Request

The final step to submitting your assignment will be to make a **pull request**. When you submit a pull request (PR for short) you are asking the owner of a repository to "pull" (and merge) your code modifications back into their repo. Although we won't be merging your submissions back into the original repo, we'll look at them and be able to review the code that you've written.

Let's get started!

1. `push` your code up to your remote repo on GitHub.com, using the command `git push origin student`.

  *At this point, your GitHub repo should show the code that you've written, and its most recent commit should be the one you just made.*

2. Go to your repo's page on GitHub (www.github.com/*your_username*/wdi-fundamentals-rps). Look at the column on the right and click where it says 'Pull Requests', and click the bright green button that says 'New Pull Request'.

3. Click the bright green button that says 'Create Pull Request'. Create a title for your pull request (anything you want); if you want, you can also add comments. When you're ready to submit the request, click 'Create Pull Request' again.

That's it! Your pull request has just been submitted.

- - - - - - - - - -

Well done! You've made it through six tough tutorials on JavaScript. Give yourself a pat on the back!

---

Now that you've finished your project, we encourage you to [learn more about GA Mentors](../07_feedback/intro.md), and how you can get feedback on your code before your course begins.
