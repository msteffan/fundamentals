**WDI Fundamentals Unit 2**

---

#####By the end of this Unit, you'll be able to:
* Define a version control system and its benefits
* Describe how Git works
* Identify the Git commands used to set up a local respository and to record snapshots
* Push local changes to a remote repository using the command line

---


#Version Control

When you’re working on a project – say a painting, a piece of software or an autobiography – there comes a time when you wish you had a reset button.

You might already have a system in place to deal with this problem – maybe you save your document multiple times with different names, so that you can return to a different stage of the project.

![Version Control](../assets/chapter2/version-control.gif)

Developers call this process “version control”.

If you're making copies of a file every time you make a change, your file system might look like this:

<br>

![Bad VCS](../assets/chapter2/bad_vcs.png)

<br>

While this method works (kinda), it has a number of major limitations.
* It's extremely duplicative - before long, you might end up with 10, 20, or even 50 slightly-different copies of the same file.
* It also only allows you to track changes in one file; if your project consists of multiple files, you're out of luck.
* Keeping track of parallel versions (revision A vs revision B).
* It's extremely difficult (if not basically impossible) to see what has changed from one version to the next without opening each file and comparing changes line by line.

Now imagine how much more complicated this process becomes once you start working with a team...

Software developers have developed a number of tools to solve the 'version control' problem for their own projects; in this course, we will focus on one particularly popular version control program called **Git**. Git addresses all of the problems mentioned above, and more; it's also an excellent tool for working collaboratively on a project, though we won't be using those features right away.

Your first step will be to install Git (if you haven't already).

##Git Installation

To install git, download the latest release from [git-scm.com](http://git-scm.com/download).

Double click on the downloaded file, and run through the installer.

You will know it worked if, when you open up the terminal and type:

```
$ git --version
```

to check to see what version of git is running, your computer returns something greater than or equal to `2.0.0`:

![Check to See What Version of Git is Running](../assets/chapter2/git_installed.gif)

---

[On to the lesson.](02_lesson.md)
