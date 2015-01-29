**WDI Fundamentals Unit 2**
---

##![Your Turn](../assets/exercise.png) Your Turn

This exercise aims to give you some practice with using the Git version control system.

1. Open up the terminal application and change to the `fundamentals` directory you created in your home directory.

2. Create a new directory inside `fundamentals` called "git-practice".

3. Use `cd` to navigate into that directory, then check to make sure the working directory has changed using the `pwd` command.

4. Use the `git init` command to create a Git repository in `git-practice`.

> **CAUTION** DO NOT create a git repository inside another git respository.  Always make sure you are initializing git within a folder whose parent directory does **not** contain a `.git` folder.

5. Notice, that there is now a `.git` directory in `git-practice` by using the `ls -a` command.

6. Create a new file called README.txt.

7. Look at the output of the `status` command; the README.txt you created should appear as an untracked file.

8. Use the `add` command to add the new file to the staging area.  Again, look at the output of the `status` command.

9. Now use the `commit` command to commit the contents of the staging area.

10. Create a directory called "src" and add a couple of files to it.

11. Use the `add` command, but name the directory, not the individual files. Use the status
command. See how both files have been staged. Commit them.

12. Make a change to one of the files. Use the `diff` command to view the details of the change.

13. Next, add the changed file, and notice how it moves to the staging area in the `status`
output. Also observe that the `diff` command you did before using add now gives no output.
Why not? What do you have to do to see a diff of the things in the staging area?

14. Now – without committing – make another change to the same file you changed in step 12.
Look at the `status` output, and the `diff` output. Notice how you can have both staged and unstaged changes, even when you’re talking about a single file. Observe the difference when you use the `add` command to stage the latest round of changes. Finally, `commit` them. You should now have started to get a feel for the staging area.

15. Use the log command in order to see all of the commits you made so far.

---

[Next : Publish Work on Github](06_lesson.md)
