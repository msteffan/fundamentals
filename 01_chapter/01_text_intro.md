##Chapter 1: A Computer Program

The **command line** is one of two ways to interact with your computer.

You could go through the rest of your life never using it. You could move your mouse, click on icons, drag and drop files from one folder to another in a state of ignorant bliss.

When you&rsquo;re using the computer this way, you&rsquo;re using what&rsquo;s called a Graphical User Interface or GUI. In a GUI (pronounced &ldquo;gooey&rdquo;), you communicate with your computer using a combination of text, images and gestures.

Command line, on the other hand, is a *text-based interface*, where you communicate with your computer using text alone.


Back in the day, the command line was the only way to interact with your computer, until the video display terminal was introduced in the mid-60s.

As a programmer, you won&rsquo;t need to revert to wearing bell-bottoms but you will need to do tasks on your computer without a mouse.


As with learning any other language –there is a learning curve.  Resist the urge to revert back to using the GUI.  

We&rsquo;ll access the command line using the Terminal (capital-T) application, the most common application on MacOSX and Linux machines.


In command line, you're communicating with your computer used 'bash' or 'shell' commands.

Later in this module, we'll be using the programming language, JavaScript.

##![Your Turn](../assets/exercise.png) Your Turn

#### The Command Line

Regular users interact with computers through a variety of mechanisms. They click on buttons, scroll through pages, drag and drop, type text, etc. Most of these operations are interacting with the computer through its Graphical User Interface, or GUI.

However, you are on a journey to transcend being an ordinary user of computers.
You are on your way to becoming a developer, and developers like to interact
with computers in a different way. They like to keep their hands on their keyboard.

The command line is another interface to interact with your computer that looks
something like this.

![Command line](../images/command_line.png)

That's right. No more buttons, no more pictures, no more menus. Only text. We
can perform actions using the command line by entering **commands**. There
is a command to perform virtually any action you can imagine on your computer!
There are commands to open an application, create new files, copy files from
one place to another, and a lot more.

> Developers sacrifice the ease and intuitive nature of a GUI for greater power, efficiency, and flexibility of the actions they can perform in a command line interface.

----

> **Note** This version of WDI Fundamentals only supports MacOS beyond this point

Go ahead an open up "Terminal" in any of the following ways.

* Navigate to your Applications folder and double-click on Terminal
* *Faster:* Press Command+Space on your keyboard to bring up a friend of ours, Spotlight.
  Spotlight is a tool that allows us to quickly find files and applications on
  our computer, but more on that later. Inside this search bar, type "Terminal",
  and select the Terminal application.

When you've opened up Terminal, and see a window similar to figure 1.1, proceed!

#### Terminal Commands

Welcome to the command line. It's not much to look at. No pictures, no fancy art
or animation. Just some text. Let's explore this brand new space. Type `hello?`
and press enter.

```
$ hello?
```

The dollar sign is just to indicate that this is a command line command. It
should not be typed by you. You should only type what follows the dollar sign
(in this case, `hello?`).

Your terminal may have responded rudely.

```
-bash: hello?: command not found
```

This is the way your computer likes to tell you that it did not understand the
command that you typed in. Remember, we have left the GUI world behind us, so we
will no longer have pretty warning messages and alert boxes. Do not worry. In
due time, as we grow comfortable in this new environment, even these cryptic
messages will be just as beautiful as any warning box you'll ever see.

Go ahead, type this into your terminal.

```
$ Where am I?
```

Again, probably a rude response.

```
-bash: Where: command not found
```

Great. We've established that our command line doesn't really understand plain English.
We will have to use commands that our command line can understand. Let's try
this one.

```
$ pwd
```

Whoa! It looks like our computer understood that one! It replied with a message.

```
/Users/corneliusfinch
```
What did we just do?

> The command `pwd` stands for "Print Working Directory".
> This command is used when we want the command line to tell us what folder (or
> directory) of our computer we are currently in.

Just like the Finder on a mac, your command line interface places you in a particular folder
of your computer. `pwd` tells you where you currently are. Usually, when you
open the Terminal application, you start off in your "home folder", which is the one
that shares the name of your username on your computer.

If we were using Finder, we'd be able to see what things (files and folders) are
present in this folder. In a CLI however, if we want to see what files and
folders exist at the current location, we need to ask for it with another command.
Let's find out what files are in the folder that we're in.

```
$ ls
```

Lo and behold, the contents of the folder you are in.

```
Applications       Desktop          Documents
Downloads          Library          Movies
Music              Pictures         Public
```

> The `ls` command, which loosely stands for "list", lists the contents of a
> folder.

It looks like there are some folders in here. Let's find out what's inside our
`Documents` folder. In order to do so, let's first navigate to the Documents
folder.

```
$ cd Documents
```

We have now navigated to the Documents folder.

> The `cd` command, which stands for "change directory", is used to navigate to
> a particular folder on your computer.

This is equivalent to double-clicking the Documents folder in Finder to "go
inside it". We can check that we're in the right place by using `pwd`.

```
$ pwd
/Users/corneliusfinch/Documents
```

Excellent! Now let's find out what's in here, using `ls`.

```
$ ls
funny_cat_picture.jpg
office_stuff
world_domination_checklist.txt
```

It looks like the `Documents` folder contains a JPG file of a funny cat, a folder
full of "office stuff", and a text file that supposedly contains a checklist for
world domination. Your `Documents` folder probably contains something different.

Now that we've investigated our `Documents` folder, let's go back up to our home
folder. Since the home folder contains the `Documents` folder, we can say that
the home folder is the "parent directory" of the `Documents` folder.

```
$ cd ..
```

> `..` (two periods, or "dot-dot") is how we say to our command line "parent
> directory".




#Version Control

When you’re working on something, say a painting, software or an autobiography, there comes a time when you wish you had a reset button.
You might already have a system in place for dealing with this problem –maybe you save your document multiple times with different names. Developers call this process a “version control system”.

The tool we'll be using for version control is called Git.  


Git saves a history of the changes you make for you –no need to keep multiple versions of a file on hand. 


Aptly named, Git is not too bright.  It needs you to tell it which files to track and how often to save a version.


How it works is this: you put Git in a folder and tell it which files to track (or to track all of the files in the folder)...


...and then every time you want to save a version –when you’ve completed the first chapter in your book –you tell Git to ‘commit’ that version to memory.


If you want to revert to an old version you can do that.  If you want to view the difference between two versions of a file, you can do that too.

###Example
Imagine you are working on a piece of code.  Let's call it version 1:

```js
var eureka = "The meaning of life is the following number"
var meaning_of_life = 42
console.log("Guys, I've figured it out. \(eureka) is \(meaning_of_life)!")
```





