**WDI Fundamentals Unit 2**

---

##Publish Work on GitHub

### What is GitHub?

GitHub is a place where developers can share their code, comment on, and review code changes.

### Create a GitHub account

Visit [github.com](https://github.com/join) and create a new account.

Images clicking through the signup process on GitHub.

## Create a new remote repository

Click on the "+" button in the top right, and create a new repository named "fundamentals".

Images clicking through the repo creation process.

## Tell your local repository about the remote one

To tell your local repostory about the one you just created on GitHub.com, add the remote URL.

Image showing where the SSH link is to select and copy the remote url.

    $ git remote add origin <remote-url>

You can think of `origin` as a nickname for the longer `remote-url` (which is harder to remember and type).

`<remote-url>` should be SSH.

**Should we describe the process of setting up SSH keys here?**

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

**WDI Fundamentals Chapter 4**

---

## What is GitHub Flow?

GitHub flow is a workflow for developers (as well as teachers and students)
that allows an administrator to integrate proposed changes to a repository.

## Fork the Repo

On GitHub.com, fork the ?? repository.

This will make a copy of the original repository and add it to your account.

This way, you can make as many changes as you like and push them to your own repository (fork)
without affecting the main repository.

## Create a feature branch

Remember branches from earlier? They allow us to make isolated experimental changes without
affecting the master branch.

To create a new branch:

    $ git branch feature-name

Where `feature-name` is the name of the branch you want to create. 

You can be in any state for any branch. By default, you are on the master branch.

To switch to the new branch you created:

    $ git checkout feature-name


If you want to do both of these steps in one command, which is common:

    $ git checkout -b feature-name

## Make your Changes

Make changes while you are on this feature branch.

Stage the changes:

    $ git add .

Commit them:

    $ git commit -m "description of what changed"

Push them:

    $ git push origin feature-name

The last argument to the `git push` command is the name of the branch that contains
your changes that you’d like to push.

## Submit a pull Request

By creating a pull request, you can ask the original repo’s owner to merge in your changes
on a particular branch.

Images showing how to submit a pull request on github.com

## Submitting Homework

You and your instructors will use the GitHub flow to submit and review homework assignments.

You will create a new pull request for each homework assignment to submit them to the main class
repo.

Diagram showing how three repos (local, class repo, fork) interact, which commands are used to
communicate with which repos.


