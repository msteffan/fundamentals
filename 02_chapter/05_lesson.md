**WDI Fundamentals Unit 2**

---

##Publish Work on GitHub

So far, we've been making "local" changes to files on our computers and committing them to our local repository.


To collaborate with others (and also to backup our files just in case our computer is out of commission) we need to connect our local repository to a "remote" repository.

> **HINT** Many developers call their repositories "repo" for short.


### What is GitHub?


GitHub is a company, famous for the platform they built to manage Git repositories in the cloud. On Github, developers can share their code, comment on it, and review code changes with each other. It's an implementation of the same Git software you installed on your computer, but it also comes with some additional features.

In a lot of ways, Github is like Dropbox. You can provide specific teammates with access to different repositories, and you can easily get a graphical representation of the versions of your files.

![Image of the user's Github home page, showing repositories, contribution timeline, and annotations of the key features]()

## Our GitHub Flow

There are a few different ways to work together on GitHub, and our class is going to use a specific order of operations to get things done.

The GA Instructional Team has put together resources for you in a remote repository on GitHub. You'll need to retrieve these files and save a copy on your computer using Git and GitHub. Eventually, when you've made changes that you'd like to share with our team, you'll have to submit those changes to our GitHub repo.

This is what our workflow looks like:
![GitHub Workflow](../assets/chapter2/github_workflow.gif)
<br><br>

>**Note** Don't worry, we are going to cover this step by step, in enough detail for you to complete the prework.

---

### 1. Forking

First, you're going to "fork" our repository on Github. Before we get there, let's talk about forking. "Forking" simply results in the creation of an identical copy of GA's GitHub repo, but which lives in *your* Github account. Your forked copy maintains a reference to the GA copy. Your copy includes all the same files, all of the commit history from anyone who previously made changes to the repo, all of the currently added issues, and more).

Forking makes sense in the context of a collaborative platform like Github. Think of it this way. Take an open-source project like Node.js (a JavaScript framework you'll learn about in class). Node is completely open-source, and you can [view the node source ](https://github.com/joyent/node) on Github (it's written in JavaScript, if the .js didn't give it away).  If you visit the main repo, you'll see that there are over 400 contributors who have made commits to Node.

Although it is open-source and anyone can read through or offer to contribute to the code, it is **maintained** by a company called Joyent. Not all of the 400+ contributors have the ability to push their changes straight to Joyent's repository. That wouldn't be very efficient. Maintaining an open source project is a lot of work, and is really important to make sure that the direction of the project best serves the community that uses it.

So... if you wanted to make a change to Node, you'd fork Joyent's repo (no need to do this now, we're just explaining the concept).

![Image showing repository and a highlight of the fork button]()

After forking the repo, you'd see an exact copy show up in your list of Github repos, and you'd have full access to do whatever you want with it.

![Image showing a list of repositories with the fork added]()

Similar to the process indicated in the diagram above, you would:

- pull it down to your local computer (using `git clone` – as you'll learn in a minute)
- make changes on your local computer, then commit them (as you learned in the last section)
- push your changes from your local computer (using `git push` – as you'll learn in a minute)
- submit a pull request to Joyent (using Github's interface – as you'll learn in a minute)  

If the maintainers like your change, they'll accept the commits that you included in your pull request, and you'd now be listed as a contributor to Node. You could also tell all of your future employers that you were an open-source contributor.

We're going to follow a similar process for the project you'll complete as part of Fundamentals.

### 2. Cloning

Don't try to follow these steps yet. In the [Unit 1 Homework](09_assessment.md), we'll get to actually doing all this. For now, just try to understand the concepts.

After we fork the repo, we still don't have a local copy on our computer. If we want to copy the *entire repo* (files and all historical commits) from our forked repo down to our computer, we can do that with a simple git command. Before we start, first open up Terminal and navigate to the folder into which you want to copy the repo.

Once you've navigated to your preferred location, you'll type `git clone https://www.github.com/<your username>/<repository name>.git`. You can find this "clone URL" by looking on the right side of your Github repository.

![Image showing where to copy the HTTPS clone URL]()

By issuing the clone command, you ask GitHub via command line for a copy of your remote repo. This copy is transferred to your local computer.

### 3 & 4. Editing and Committing

We covered this in the previous section. As you complete the exercises in the rest of Fundamentals, you'll do this step frequently.

### 5. Pushing

Once committed some added or edited files to your local repo, you'll want to synchronize those changes back up to your remote GitHub repo. From Terminal, and within your directory, you'll type `git push origin master`. Pushing does not happen automatically – until you type those words, GitHub does not know about your commits. After you type those words, Github has a copy of all of the commits you've made.

Don't worry too much about the origin and master part, for now. In brief:

- `origin` is the name of your default **remote** (in this case Github). You can have many remotes, if you want. We're not going to cover that use case right now.

- `master` is the name of the **branch** you're on. You'll make use of branches consistently in your class. Again, we're not going to cover them as part of Fundamentals, but you can read up on them later if you wish. For now, we're just going to be doing our work on the `master` branch.

### 6. Submitting a Pull Request

Once your changes are in your remote repository on Github, you can send a **pull request** to the original repository your forked. A pull request is effectively saying "Hello maintainer of project X, I made some changes here in my forked copy and I think they're pretty good. You should pull them back into your repository."  This is a GitHub feature, so you'll need to head back to the browser to make this happen.

A pull request has three major parts:
- **Source branch** (on your forked repo)
- **Destination branch** (the original repo)
- **Title** (a description of what changes were made)
- **Description** (more info that can help the repository maintainers decide if they want to accept the pull request)

## Homework and Assignments on GitHub

For now, that's all you need to know.

We'll revisit Git and Github again and again. 

At the end of this book, we will ask you to submit a pull request with your Fundamentals project. During WDI, your instructors will probably use a similar GitHub workflow to have you access new assignments and submit your answers back.

## Confused?

If you ever get stuck working with Git or GitHub, don't worry, you are NOT the first. When you don't understand something, we encourage you to follow a three-step process:

1. Search online for an answer (via Google or [Stack Overflow](www.stackoverflow.com))
2. Ask classmates if they've solved a similar problem (via [Slack](ga-students.slack.com/wdi-fundamentals))
3. Go to an instructor for help (instructors are also on Slack)

And trust us... you *will* get to the point where cloning and pulling are like breathing and sleeping.

---

Ready for another quiz? [Here we go!](05_quiz.md)



