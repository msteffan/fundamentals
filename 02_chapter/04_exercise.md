**WDI Fundamentals Unit 2**

---

##![Your Turn](../assets/exercise.png) Your Turn

This exercise will give you some practice using Git.

1. Open your terminal and go into to the `fundamentals` directory you created earlier. Create a new directory inside it called "git-practice".

2. Use `cd` to navigate into that new directory; you can make sure you're in the right place by using the `pwd` command.

3. Use `git init` to create a Git repository in the `git-practice` directory.

   <br>

  > **CAUTION** Before running `git init`, make sure you're not already inside another Git repository. Type `git status`. If you see `fatal: Not a git repository (or any of the parent directories): .git`, then you know you're good to go, and you can safely run `git init` within this folder.

  Notice that there is now a `.git` directory in `git-practice` - you'll see it if you run the `ls -a` command.

4. Create a new file called `README.txt` and run `git status`. What output do you get?

5. Use the `git add` command to add the new file to the staging area.  Run `git status` again - how has the output changed?

6. Now that you're satisfied with the changes that you've staged, commit them using <code>git commit -m "..."</code>. Give the commit an appropriate message - remember, it should be short but descriptive.

7. Create a directory called `src` and add a couple of files to it.

8. Use the `add` command, but add the `src` directory instead of the individual files. Use the `git status`
command - see how both files have been staged? Go ahead and commit the addition of these new files to the repo.

9. Make a change to one of the files, and run `git diff` to look at all the unstaged changes to our repo. What do you see?

10. Next, `add` the changed file and type `git diff` What's changed? Why? What do you have to do to see a `diff` of the things in the staging area?

11. Now – without adding or committing – make another change to the same file you changed in step 9. Look at the `status` output, and the `diff` output. See how you can have both staged and unstaged changes, even when you’re talking about a single file?

12. Finally, `add` and `commit` all outstanding changes. Use the `log` command to see all of the commits you've made so far.

---

[Next Up: Publish Work on Github](05_lesson.md)
