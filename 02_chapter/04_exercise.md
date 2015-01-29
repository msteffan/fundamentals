**WDI Fundamentals Unit 2**
---

##![Your Turn](../assets/exercise.png) Your Turn

This exercise aims to give you some practice with using the Git version control system.

> **HINT** When you create new repositories and directories, you can keep them wherever you want, but it's often a good idea to create a `development` folder inside your home directory and store all your code repos in there. It doesn't have to be called `development`, you could just as well name it something else. It's just a good idea to keep them somewhere consistent.

1. Open up the terminal application and create a directory called `wdi-fundamentals-practice`.

1. Use `cd` to navigate into that directory, then check to make sure the working directory has changed using the `pwd` command.

1. Use the `git init` command to create a Git repository in that directory.

1. Notice, that there is now a `.git` directory by using the `ls -a` command.

1. Create a new file called README.txt.

1. Look at the output of the `status` command; the README.txt you created should appear as an untracked file.

1. Use the `add` command to add the new file to the staging area.  Again, look at the output of the `status` command.

1. Now use the `commit` command to commit the contents of the staging area.

1. Create a directory called "src" and add a couple of files to it.

1. Use the `add` command, but name the directory, not the individual files. Use the status
command. See how both files have been staged. Commit them.

1. Make a change to one of the files. Use the `diff` command to view the details of the change.

1. Next, add the changed file, and notice how it moves to the staging area in the `status`
output. Also observe that the `diff` command you did before using add now gives no output.
Why not? What do you have to do to see a diff of the things in the staging area?

1. Now – without committing – make another change to the same file you changed in step 10.
Look at the `status` output, and the `diff` output. Notice how you can have both staged and
unstaged changes, even when you’re talking about a single file. Observe the difference when
you use the `add` command to stage the latest round of changes. Finally, `commit` them. You
should now have started to get a feel for the staging area.

13. Use the log command in order to see all of the commits you made so far.

---

[Next : Publish Work on Github](06_lesson.md)
