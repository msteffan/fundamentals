**WDI Fundamentals Chapter 2**

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

Many people's version control system of choice
is to copy entire directories before making 
changes to an existing project.

Often, they will add a time, date, or version number to the copied folder to identify which folder contains which changes.

You might end up with a file system that looks like:

![](http://updog.co/img/files.png)

While this method works, it is impossible to see
what has changed in each version without opening each file and comparing changes line by line.

Additionally, it requires you to remember which folder you're working before saving further changes.

If you're working with others on a project, the process of referring to versions is extremely error-prone, and it becomes increasingly difficult to collaborate on a project.


## Distributed Version Control Systems

One solution to the aformentioned problem is a distributed version control system.

A distributed system means that each copy of a project contains the entire history of the project.

If one collaborator loses her changes, she can get back her work by making a copy of one of the existing projects.

The tool we'll be using for version control is called Git.  

Git saves a history of the changes you make for you –no need to keep multiple versions of a file on hand. 

Aptly named, Git is not too bright.  It needs you to tell it which files to track and how often to save a version.


How it works is this: you put Git in a folder and tell it which files to track (or to track all of the files in the folder)...


...and then every time you want to save a version –when you’ve completed the first chapter in your book –you tell Git to ‘commit’ that version to memory.


If you want to revert to an old version you can do that.  If you want to view the difference between two versions of a file, you can do that too.


While there are many distributed version control systems, we'll be using git for its speed, efficiency and popularity among developers.
