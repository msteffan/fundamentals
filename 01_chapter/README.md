**WDI Fundamentals Unit 1**
---
By the end of this Unit, you'll be able to:

* Differentiate between a command line interface and a graphical user interface
* Summarize a basic filesystem structure
* Open a file in a text editor and make changes from the command line
* Identify when you might want to use absolute versus relative paths

##Thinking like a Programmer

Most computer users move their mouse, click on icons, drag and drop files from one folder to another.

When you&rsquo;re using the computer this way, you&rsquo;re using what&rsquo;s called a Graphical User Interface or GUI. In a GUI (pronounced &ldquo;gooey&rdquo;), you communicate with your computer using a combination of text, images and gestures.

You are on a journey to transcend being an ordinary user of computers.
You are on your way to becoming a developer, and developers like to interact with computers in a different way –through the command line.

Unlike the GUI, the command line is a *text-based interface*, where you communicate with your computer using text alone.

Back in the day, the command line was the only way to interact with your computer, until the video display terminal was introduced in the mid-60s.

We can perform actions using the command line by **entering commands**. There is a command to perform virtually any action you can imagine on your computer!
There are commands to open an application, create new files, copy files from one place to another, and a lot more.

We&rsquo;ll access the command line using the Terminal (capital-T) application, the most common application on MacOSX and Linux machines.

> **NOTE**: Fundamentals will not explore the command line that comes with Windows, because most developers don&rsquo;t use it. If you&rsquo;re a Windows user, we recommended installing a command line program like <a href="http://cygwin.com/" target="_blank" >Cygwin</a> or <a href="http://msysgit.github.io/" target="_blank">MSysGit</a> in order to follow along with the syntax we use here.

##Get Started Using Terminal

When you open Terminal, you should see a window like this:

<img src="../assets/Graphics/terminal_blank.gif" alt="Blank Console">

This window is where you&rsquo;ll tell the computer what to do, and where the computer will display its reply.

The <strong>prompt</strong> is the &lsquo;$&rsquo; that automatically shows up on the end of the first line. It&rsquo;s the command line equivalent of &lsquo;stand-by&rsquo; and indicates Terminal is ready to accept your <a href="#command"><strong>command</strong></a>. We&rsquo;ll learn a few commands later in this lesson.

The <strong>cursor</strong> follows the prompt and the text you type will appear here.

Just like in every other setting where you've ever seen a cursor.

The <strong>username</strong> of the person logged in precedes the prompt, and as you can see above, this user is named <em>samspade</em>.
