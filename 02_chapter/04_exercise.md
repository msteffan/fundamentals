**WDI Fundamentals Unit 2**

---

##![Your Turn](../assets/exercise.png) Your Turn

This exercise will give you some practice using Git.

1. Open your terminal and go into to the `fundamentals` directory you created earlier. Create a new directory inside it called "git-practice".

2. Use `cd` to navigate into that new directory; you can make sure you're in the right place by using the `pwd` command.

4. Use `git init` to create a Git repository in the `git-practice` directory.
      > **WARNING**: DO NOT create a Git repository inside another Git repository.  Always make sure you are initializing Git within a folder whose parent directory does **not** contain a `.git` folder.
  Notice that there is now a `.git` directory in `git-practice` - you can see by using the `ls -a` command.

5. Create a new file called `README.txt` and run `git status`. What output do you get?

6. Use the `add` command to add the new file to the staging area.  Run `git status` again - how has the output changed?

7. Now that you're satisfied with the changes that you've staged, commit them using <code>git commit -m "..."</code>. Give the commit an appropriate message - remember, it should be short but descriptive.

8. Create a directory called "src" and add a couple of files to it.

9. Use the `add` command, but add the `src` directory instead of the individual files. Use the status
command - see how both files have been staged? Go ahead and commit the addition of these new files to the repo.

10. Make a change to one of the files, and run `git diff` to look at all the unstaged changes to our repo. What do you see?

11. Next, `add` the changed file and type `git diff` What's changed? Why? What do you have to do to see a `diff` of the things in the staging area?

12. Now – without adding or committing – make another change to the same file you changed in step 12. Look at the `status` output, and the `diff` output. See how you can have both staged and unstaged changes, even when you’re talking about a single file?

15. Finally, `add` and `commit` all outstanding changes. Use the `log` command to see all of the commits you made so far.

---

[Next : Publish Work on Github](05_lesson.md)

