**WDI Fundamentals Chapter 5**

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

