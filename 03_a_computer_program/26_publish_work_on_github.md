**Publish Work on GitHub**

---

## What is GitHub?

GitHub is a place where developers can share their code, comment on, and review code changes.

## Create a GitHub account

Images clicking through the signup process on GitHub.

## Create a new remote repository

Images clicking through the repo creation process.

## Tell your local repository about the remote one

To tell your local repostory about the one you just created on GitHub.com, add the remote URL.

Image showing where the SSH link is to select and copy the remote url.

    $ git remote add origin <remote-url>

You can think of `origin` as a nickname for the longer `remote-url` (which is harder to remember and type).

`<remote-url>` should be SSH.

Should we describe the process of setting up SSH keys here?

HTTPS will work, but students will have to type in their username and password each time
they communicate with GitHub.com from the command line.

## Push your changes

To push your local changes to the new remote repository, use `git push`:

    $ git push origin master

`master` is the name of the branch that you want to push.

## What’s a Branch?

A branch in git is like an alternate universe. You can create many different branches
to experiment with different features or bug fixes in an isolated environment that
contains only those changes.

Should we talk more about branches?



