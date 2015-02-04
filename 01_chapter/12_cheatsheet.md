**WDI Fundamentals Unit 1**

---

##Command Line CheatSheet

####Command Line
* A text-based interface.
* *Synonyms*: command-line interface (CLI), console

####Terminal
* An OSX application that provides text-based access to the operating system;
* Any device or application used for data entry and display in a computer system
* *Synonyms*: client, computer terminal, terminal emulator

####File System
* A file system is a systematic way to control how information is stored and retrieved. It describes where one piece of information stops and where the next one begins. Each file system has its own structure and logic.
* *Synonyms*: NTFS (Windows' File System), HFS+ (Apple's File System), file allocation table, GFS (Global File System)

####Directory
* An organizational unit, or container, used to organize computer files into a hierarchical structure.
* *Synonyms*: folder, catalog, drawer

####Path
* A sequence of symbols and names that identifies a file or directory. The path always starts from your working directory or from the root directory, and each subdirectory is followed by a forward slash.
* An *absolute* or full path begins with the root directory and specifies every directory above the terminating file or dirctory name.
* A *relative* path does not include the root or parent directory names, and refers to a file or directory directly below the current working directory.
* *Synonyms*: pathname

####Command
* The action we want the computer to take; always a single word.
* *Synonyms*: utility

####Option
* Follows the "command" in a command line, to modify the behavior of the command in some way.
* *Synonyms*: flag

####Argument
* Follows the "command" and "options" (if any) in a command line, and is used to explain what we want the command to act on.
* The number of arguments used generally depends on the command: some don't need arguments, some require exactly one argument, some require lots of arguments, and some are flexible in the number they can take.

Command | Description
---|---
`pwd -options` | Prints the working directory; returns the absolute path name of the current directory.
`ls [-options] [path/to/directory]` | Lists directory contents.
`cd [-options] [path/to/directory]` | Changes the current working directory to the specificed directory.
`mkdir [-options] [path/to/directory]` | Makes a new directory
`rm -r [path/to/file] [path/to/file] ... ` | Removes directories or files permanently
`mv [-options] [path/to/file] [path/to/directory]` | Moves directories or files to a new local
`mv [-options] [path/to/file] [NEW_FILE_NAME]` | Renames a file or directory.


Your Terminal comes with a manual, and to access more (*a lot more*) information about any command, type <code>man</code> followed by the command name and press <kbd>Enter</kbd>:
	
![manual](../assets/chapter1/terminal_man.gif) 

You can scroll through a manual entry with the arrow keys or space bar. To quit this view and return to your prompt, just type <code>q</code>.


