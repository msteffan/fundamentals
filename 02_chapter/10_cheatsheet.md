**WDI Fundamentals Unit 2**

---

# Git Cheat Sheet

Command | Description
---|---
`git init` | Tells Git to start monitoring the current folder you're in. In other words, for my `pwd`, create a new "timeline" where we can manage our source code.
`git diff path/to/file` _[can take a directory or file]_ | Show the changes of the given file or directory.
`git add path/to/file` _[can take a directory or file]_ | Add a file to the "stage". The stage can be thought of as an inbetween state between the last commit and what is ready to be committed. Once the command `git commit` is run, all staged files will be committed to the timeline.
`git status` | Get the current status of Git. Files that are "staged" (about to be committed), and files that are unstaged (files that have changed since the last commit, but are not about to be committed) will both show up here
`git commit -m "Commit message"` | Commit all staged files to the timeline. If `-m "Commit messsage"` is ommitted, Git will open your default text editor (typically Vim) to enter a longer message. If for any reason Vim is opened, you can close it by typing `:q`.
`git log` | Visualize the timeline. You can scroll with the arrow keys or `j`, `k`, and it can be exited by typing `q`.
