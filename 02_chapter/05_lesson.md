**WDI Fundamentals Unit 2**

---

##Publish Work on GitHub

So far, we've been making changes "locally" - editing files and repositories on our computers.

To collaborate with others (and also to backup our files just in case our computer is out of commission) we need to connect our local repository to a "remote" repository.

### What is GitHub?

GitHub is a company, famous for the platform they built to manage Git repositories in the cloud. On Github, developers can share their code, comment on it, and review code changes with each other. It's an implementation of the same Git software you installed on your computer, but it also comes with some additional features.

In a lot of ways, Github is like Dropbox. 

You have a folder in the cloud, your *remote repo*, which syncs with your computer. You can share this remote repo with others, grant them special permissions, and you can view different versions of your files.

Below is what the Github interface looks like for a repo called `awesome-project`:

![Github Interface](../assets/chapter2/github.gif)

1. **Repo Name and Owner** - describes who owns the repository, what the name of the repo is and whether the repo is public or private.

2. **Overview** - displays the number of commits, branches, releases and contributors to a particular repo.  Selecting any one of these options will bring a detailed view of that selection.

3. **Repo File Structure** - displays the contents of the repo.  Selecting any file or folder will open a detailed view of that file and allow you to edit the content directly.

4. **Fork button** - allows you copy a version of this repo (`user/awesome-project`) to your own Github account.

5. **Side Bar** - use the side bar to respond to issues, create pull requests, and change the settings for this repo.

There are a ton of unique Github features crammed on this page, but we'll only be using three of them to start.


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

First, you're going to **fork** our repository on Github by clicking the button we highlighted above. 

> **CAUTION** Don't follow these steps just yet. Read this chapter and then you'll have a chance to try it out yourself in the [Unit 2 Homework](09_assessment.md).

"Forking" adds a copy of someone else's GitHub repo to *your* Github account. 

The forked repo is not perfectly identical - but it includes all the same source files, issues, and commit history.

![Forking GIF](../assets/chapter2/fork_node.gif)

Let's walk through an example. Consider a project like Node.js, a JavaScript framework that you'll learn about in class. Node.js is completely open-source, which means that anyone can read (and even copy) the code that makes it work - including you! The source code is publicly available [here](https://github.com/joyent/node) on Github; if you visit the main repo, you'll see that there are over 400 contributors who have made committed changes to Node.js.

![Node.js Contributors](../assets/chapter2/node.png)

Although it is open-source and anyone can read or contribute to the code, it is **maintained** by a company called Joyent. Not all of the 400+ contributors have the ability to edit the original Joyant repo – that wouldn't be very efficient or safe. Someone could accidentally make a change that conflicts with someone else's contributions, causing things to break. Changes need to be inspected and approved before they can officially be added to the project.

By forking Joyent's repo, you could have a full working copy of the Node.js source code to play with. When you break something, which you will, everyone does, Node.js won't be affected.


### 2. Cloning

Next, after you've forked our repo, you'll want to place a local copy on your computer. 

To copy your fork down to your computer, you'll need to open up the Terminal and use a Git command.

You need to navigate to the place where you'd like to store the repo, and then type:
```
git clone <clone URL>
```
You can find the `<clone URL>` on right side of your Github repository:

![Node.js Clone](../assets/chapter2/node_clone.png)

By issuing the clone command, you ask GitHub via command line for a copy of your remote repo, and this copy or **clone** ends up in your working directory.


### 3 & 4. Editing and Committing

We covered this in the previous section. As you complete the exercises in the rest of Fundamentals, you'll need to do this step frequently.

### 5. Pushing

Once you've committed the changes you've made to the code, your local repo will be different from your remote repo; to update your remote repo on GitHub, you have to **push** those changes, using the Git command `git push origin master`.

Don't worry about the `origin` and `master` part just yet. 

If you're curious, here's a brief overview:
* `origin` is a shortcut for the URL of your default remote repo (in this case, the repo on Github). You can have many remotes, if you want. We're not going to work with more than one in Fundamentals.
* `master` refers to the **branch** on your remote repo where you're currently adding your changes. Again, for now, we're just going to be doing our work on the `master` branch. 


### 6. Submitting a Pull Request

Once your changes are pushed to your remote repository on Github, you can notify GA of your changes by submitting a **pull request** to our original repo. 

A pull request is effectively saying "Hello maintainer of project X, I made some changes here in my forked copy and I think they're pretty good. You should add them to your repository."  Pull requests are a GitHub feature, so you'll need to head back to the browser to make this happen.

We're going to cover how to submit a pull request in a later chapter.

> **NOTE** At the end of this book, we will ask you to submit a pull request with your Fundamentals project. During WDI, your instructors will probably use a similar GitHub workflow to have you access new assignments and submit your answers back.

## Confused?

If you ever get stuck working with Git or GitHub, don't worry, you are NOT the first. When you don't understand something, we encourage you to follow a three-step process:

1. Search online for an answer (via Google or [Stack Overflow](www.stackoverflow.com))
2. Ask classmates if they've solved a similar problem (via [Slack](ga-students.slack.com/wdi-fundamentals))
3. Go to an instructor for help (instructors are also on Slack)

And trust us... you *will* get to the point where cloning and pushing are like breathing and sleeping.

---
Ready for another quiz? [Let's go.](06_quiz.md)
