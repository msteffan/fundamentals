# Know Your Computer - Exercise

## Objectives

* Practice utilizing common command line commands
* Practice utilizing keyboard shortcuts

Throughout these modules, we are going to work one step at a time towards
building our first programming project! With our newly learned computer
efficiency skills, let's set up our project folder with all the necessary files
to get started.

Here is the file structure that we want to have at the end of this exercise to
set up for our first project.

**WORK IN YOUR NITROUS BOX FOR THIS EXERCISE**

```
workspace
└── wdi
    └── fundamentals
        └── project_todo
            ├── main.rb
            └── readme.md
```

The `workspace` folder should already exist on your Nitrous box.

Inside `workspace`, we are going to create a `wdi` folder. This folder is
going to contain a `fundamentals` folder. You can put other work related to
the fundamentals material in here as well.

Of importance to us right now, the `fundamentals` folder is going to contain a
`project_todo` folder, inside which we are going to create our project files. The first
file we need is `main.rb`. The `.rb` extension indicates that the file is a ruby
program/script.

The second file is `readme.md`. The `.md` extension indicates that the file is a
Markdown file. [Markdown](http://en.wikipedia.org/wiki/Markdown) is an elegant
way of created structured text files, using a special syntax.

Of course, in the interest of learning, we are going to take a few detours along
the way to achieving this file structure to get as much practice with our newly
acquired command line and keyboard skills.

Let's get started.

## Task

For this exercise, there is one golden rule that you must follow. Stated simply,

**YOU MAY NOT TOUCH YOUR MOUSE**

That's the only one. Here we go.

#### Phase 1

1. Create the `wdi` and `fundamentals` folders in the appropriate places
1. In the `wdi` folder, create a folder called `project_todo`
1. In the `project_todo` folder, create two files: `main.txt` and `readme.txt`

#### Phase 2

1. Navigate back to the `wdi` folder
1. In the `wdi`, create another folder called `project_done`
1. In the `project_done` folder, create a file called `readme.txt`

#### Phase 3

1. Navigate back to the `wdi` folder
1. Copy the `project_todo` folder into the `fundamentals` folder
1. Delete `project_todo` and `project_done` in the `wdi` folder

#### Phase 4

1. Navigate to the `project_todo` folder that exists inside `fundamentals`
1. Open `main.txt` and add the text `puts "Hi there!"`. Make sure to be exact.
1. Save and close `main.txt`
1. Open `readme.txt` and add the text `Welcome to our first project.`. (On Nitrous,
   we cannot open files with the `open` command, so you may use your mouse to navigate
   the file structure and open up files in the Nitrous text editor)
1. Save and close `readme.txt`
1. Rename `main.txt` to `main.rb` by using the `mv` command (you need to "move"
   `main.txt` to a file with the name `main.rb`)
1. Rename `readme.txt` to `readme.md` by using the `mv` command (you need to "move"
   `readme.txt` to a file with the name `readme.md`)

We are now ready to go!
