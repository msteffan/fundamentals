**WDI Fundamentals Chapter 2**

---

## Tracking Changes with Git


###Initializing your first repository

To start tracking changes, change directories to an existing
folder on your system:

    $ cd fundamentals/

Initialize the repository:

    $ git init

This command will create a hidden folder named `.git/`, which contains the
data for the history of your entire project.

### Staging and Committing Changes

To see what git knows about your project, run:

    $ git status

Reading the output of this command will tell you that you have several untracked files.
To start tracking these files:

    $ git add .

If you now run

    $ git status

You’ll see `Changes to be committed:`

The files you have started tracking with `git add .` are now in the staging area,
which is a temporary place that allows you to commit only the changes you want in your history.

Wouldn’t you want to save all the changes you make every time you commit? No!

Sometimes you make several changes all over the place, but only want to share your work on a few files
with others.

^^ Relate this to previous examples.

To commit these changes to your repository:

    $ git commit -m "message explaining what changes you made"

The `-m` option allows you to supply a message containing a description of the changes you made.

You should commit as often as possible, as you can go back to the state of your project at any given commit.