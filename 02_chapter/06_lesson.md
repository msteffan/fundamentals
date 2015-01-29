**WDI Fundamentals Unit 2**

---

##Publish Work on GitHub

So far, we've been making changes to files on our computers, what are known as "local" changes.  

To share our work with others (and also to backup our files just in case our computer is out of commission) we need to set up "remote" repositories.


### What is GitHub?

GitHub is a company, famous for the platform they built to manage Git repositories remotely in the cloud.

Github is a lot like Dropbox –thought it's much a more powerful collaboration tool. On Github, developers can not only host and share their code, they can also comment on other people's code, review changes and edit directly in the browser.


## Our GitHub Flow

There are a few different ways to work together on GitHub, and our class is going to use a specific order of operations to get things done.

The GA Instructional Team has put together resources for you in a remote repository on GitHub –and you'll need to retrieve these files and save a copy on your computer using Git and GitHub.

Eventually, when you've made changes that you'd like to share with our team, you'll have to submit those changes to our GitHub repo.

This is what our workflow looks like:
![GitHub Workflow](../assets/chapter2/github_workflow.gif)

Don't worry, we'll go through this step by step.  

---

### 1. Forking

First, to make a copy of GA's GitHub repo (including the files, commit history, issues, and more), you need to **fork** it on GitHub.  

Once you fork GA's repository, this copy (also called a fork) now lives in your GitHub account.  Nothing has yet happened to your local computer.

This way, you can make as many changes as you like and push them to your own repository/fork without affecting the original repository.

### 2. Cloning

Next, you need to copy the files from your fork down to your computer. You do this by opening up the terminal application and typing `git clone <>`.

You're asking GitHub via command line for a copy of your remote repo. The repo is now stored on your local computer.

### 5. Pushing

You should already know how to make changes to a file or folder locally, and then add and commit those changes using `git add .` and `git commit -m "various reasons"`.

Now it's time to sync your remote GitHub repo with the changes you've made. You need to open up command line again, and type `git push origin master`.  Pushing does not happen automatically –until you type those words, GitHub does not know about your commits.

### 6. Submiting a pull Request

We'd love to see your work, and so to share the contents of your remote repo with us, you can send us a **pull request**.  This is a GitHub feature, so you'll need to head back to the browser.

##Homework and Assignments on GitHub

During WDI, your instructors will use this GitHub workflow to post new assignments and you will submit your homework using a pull request. 

At the end of this book you'll be asked to submit a pull request with your final project, and our instructional team will review them all. If you ever get stuck working with Git or GitHub, don't worry, you are NOT the first.  

Please reach out to your [GA Mentor]() or your classmates on Slack, and together we will get to a point where pushing and pulling are as intuitive to you as breathing. 

Ready for another [quiz](07_quiz.md)?


