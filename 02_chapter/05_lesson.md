**WDI Fundamentals - Unit 2**

---

##Publish Work on GitHub

So far, we've been making changes "locally" - editing files and repositories on our computers.

To collaborate with others (and also to backup our files just in case our computer is out of commission) we need to connect our local repository to a "remote" repository.

### What is GitHub?

GitHub is a company, famous for the platform they built to manage Git repositories in the cloud. On Github, developers can share their code, comment on it, and review code changes with each other. It's an implementation of the same Git software you installed on your computer, but it also comes with some additional features.

In a lot of ways, Github is like Dropbox. You can provide specific teammates with access to different repositories and you can easily get a graphical representation of the versions of your files.

![Github Interface](../assets/chapter2/github.gif)

1. **Repo Name and Owner** - describes who owns the repository, what the name of the repo is and whether the repo is public or private.

2. **Overview** - displays the number of commits, branches, releases and contributors to a particular repo.  Selecting any one of these options will bring a detailed view of that selection.

3. **Repo File Structure** - displays the contents of the repo.  Selecting any file or folder will open a detailed view of that file and allow you to edit the content directly.

4. **Fork button** - allows you copy a version of this repo (`user/awesome-project`) to your own Github account.

5. **Side Bar** - use the side bar to respond to issues, create pull requests, and change the settings for this repo.



## Our GitHub Flow

There are a few different ways to work together on GitHub, and our class is going to use a specific order of operations to get things done.

The GA Instructional Team has put together some resources for you in a repository on GitHub; you'll need to retrieve these files and save a copy on your computer using Git. 

Eventually, when you've made changes that you'd like to share with our team, you can to submit those changes back to us via our GitHub repo.

This is what our workflow looks like:
![GitHub Workflow](../assets/chapter2/github_workflow.gif)
<br><br>


**Don't worry**, we are going to cover this step by step, in plenty of detail.

---

### 1. Forking

First, you're going to "fork" our repository on Github. "Forking" simply means creating a copy of someone else's GitHub repo, and associating it with *your* Github account. 

The forked repo is not perfectly identical - but it includes all the same source files, issues, and commit history.

Forking makes sense in the context of a collaborative platform like Github. Consider a project like Node.js, a JavaScript framework that you'll learn about in class. Node is completely open-source, which means that anyone can read (and even copy) the code that makes Node work - including you! Node's source code is available [here](https://github.com/joyent/node) on Github; if you visit the main repo, you'll see that there are over 400 contributors who have made commits to Node.

Although it is open-source and anyone can read through or offer to contribute to the code, it is **maintained** by a company called Joyent. Not all of the 400+ contributors have the ability to push their changes straight to Joyent's repository. That wouldn't be very efficient or safe - someone could accidentally make a change that conflicts with someone else's contributions, causing things to break. Changes need to be inspected and curated before they can officially be added to the project.

This is where forks come in. By forking Joyent's repo, you could have a full working copy of the Node source code to play with. But even if you break something, Node's codebase won't be affected.



Once a repo is forked, it gets added to the list of repositories associated with your GitHub account. To actually make changes to the code, you would need to:

- 'clone' (copy) your GitHub repo down to your local computer
- make changes to your local copy and commit them
- 'push' your changes back from your local computer to your repo on GitHub
- ask Joyent to accept and 'pull' the changes from your fork into their project via a 'pull request', part of GitHub's interface

If Joyent likes your change, they'll accept the commits that you included in your pull request, and you'd now be listed as a contributor to Node. You could also tell all of your future employers that you were an open-source contributor!

We're going to follow a similar process for the project you'll complete as part of Fundamentals.

### 2. Cloning

Don't try to follow these steps yet. In the [Unit 1 Homework](09_assessment.md), we'll get to actually doing all this. For now, just try to understand the concepts.

After we fork the repo, we still don't have a local copy on our computer. If we want to copy the *entire repo* (files and all historical commits) from our forked repo down to our computer, we can do that with a simple Git command. Before we start, first open up Terminal and navigate to the folder into which you want to copy the repo.

Once you've navigated to your preferred location, type `git clone https://www.github.com/<your username>/<repository name>.git`. You can find the entire "clone URL" by looking on the right side of your Github repository.

![Image showing where to copy the HTTPS clone URL - IMAGE NEEEDED]()

By issuing the clone command, you ask GitHub via command line for a copy of your remote repo. This copy is transferred to your local computer.

### 3 & 4. Editing and Committing

We covered this in the previous section. As you complete the exercises in the rest of Fundamentals, you'll do this step frequently.

### 5. Pushing

Once you've committed your changes, your local repo will be different from your remote repo; to add the new changes to your remote repo on GitHub, you have to 'push' those changes, using the Git command `git push origin master`.

You don't have to worry too much about the origin and master part just yet, but here's a brief overview:
* `origin` is a shortcut for the URL of your default remote repo (in this case, the repo on Github). You can have many remotes, if you want. We're not going to cover that use case right now.

*`master` refers to the **branch** on your remote repo where you're currently adding your changes. You'll make use of branches consistently in your class. We're not going to cover them as part of Fundamentals, but you can read up on them later if you wish; for now, we're just going to be doing our work on the `master` branch.

### 6. Submitting a Pull Request

Once your changes are in your remote repository on Github, you can send a **pull request** to the original repository your forked. A pull request is effectively saying "Hello maintainer of project X, I made some changes here in my forked copy and I think they're pretty good. You should pull them back into your repository."  This is a GitHub feature, so you'll need to head back to the browser to make this happen.

A pull request has three major parts:
- **Source branch** (the branch that you're copying from, on your forked repo)
- **Destination branch** (the branch that you're copying to, the original repo)
- **Title** (a description of what changes were made)
- **Description** (more info that can help the repository maintainers decide if they want to accept the pull request)

> **NOTE** At the end of this book, we will ask you to submit a pull request with your Fundamentals project. During WDI, your instructors will probably use a similar GitHub workflow to have you access new assignments and submit your answers back.

## Confused?

If you ever get stuck working with Git or GitHub, don't worry, you are NOT the first. When you don't understand something, we encourage you to follow a three-step process:

1. Search online for an answer (via Google or [Stack Overflow](www.stackoverflow.com))
2. Ask classmates if they've solved a similar problem (via [Slack](ga-students.slack.com/wdi-fundamentals))
3. Go to an instructor for help (instructors are also on Slack)

And trust us... you *will* get to the point where cloning and pulling are like breathing and sleeping.

---
Ready for another quiz? [Let's go.](06_quiz.md)
