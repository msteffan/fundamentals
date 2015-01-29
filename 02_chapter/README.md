**WDI Fundamentals Unit 2**

---

#####By the end of this Unit, you'll be able to:
* Define a version control system and it's benefits
* Describe how Git works
* Identify the Git commands used to set up a local respository and to record snapshots
* Update a remote repository with local changes to a text file, from the command line

---


#Version Control

When you’re working on something, say a painting, software or an autobiography, there comes a time when you wish you had a reset button.

You might already have a system in place to deal with this problem –maybe you save your document multiple times with different names, so that you can return to a different stage of the project.

![Version Control](../assets/chapter2/version-control.gif)

Developers call this process a “version control system”.

If you're making copies of a file every time you make a change, your file system might look like this:

<br>

![Bad VCS](../assets/chapter2/bad_vcs.png)

<br>

While this method works, it is impossible to see
what has changed in each version without opening each file and comparing changes line by line.

Organizing different versions of your files gets even more complicated once you start working with a team.

To solve these problems, we are going to use the popular version control system called **Git**.

Git saves a history of the changes you make for you –no need to keep multiple versions of a file on hand. Git is also an excellent tool for working collaboratively on a project, though we won't be using those features right away.

Next, you'll need to (if you haven't already).

##Git Installation

Git is a distributed version control tool that allows developers to manage versions of their code over time and facilitates collaboration between several people who might be working on the same project.

Distributed means that each copy of any repostitory contains the entire history of the project.

To install git, download the latest release from [git-scm.com](http://git-scm.com/download).

Double click on the downloaded file, and run through the installer.

You will know it worked if, when you open up the terminal and type:

```
$ git --version
```

to check to see what version of git is running, your computer returns something greater than or equal to `2.0.0`:

![Check to See What Version of Git is Running](../assets/chapter2/git_installed.gif)

---

[On to the next lesson.](02_lesson.md)
