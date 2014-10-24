**Know Your Computer**

---

#### Absolute and Relative paths

* Two ways to specify paths
  * Relative
  * Absolute

We have been using relative paths so far. You specify where you want to go
relative to where you are now. "I want to go 4 blocks South".

Absolute paths specify where you want to go by exact location. "I want to go
to the corner of 34th Street and 8th Ave."

Absolute paths **always** start with a `/`. For example, `/Users/corneliusfinch`.

Relative paths **never** start with a `/`. For example, `Pictures`.

---

#### Creating files and folders

We now know how to find our way around this mysterious world called the command
line. Let's perform some lasting actions, like creating some files and folders.
Before we start, let's make sure that we are in our home folder like so.

```
$ cd ~
```

> `~` (tilde) is a shortcut to refer to your home folder.

The above command, regardless of where we currently are, will take us to our
home folder. Great! Now that we're here, let's create a file.

```
$ touch joke.txt
```

> The `touch` command creates files for us. If we try to "touch" a file that
> already exists, it will not be overwritten.

We made a text file called `joke.txt`! Let's open it up in our default text editor so we can write a joke in it. Can we do that from our command line? Of course!

```
$ open joke.txt
```

Your text editor should open up this file now. Go ahead and type a joke in
there, save that file, quit your text editor application, and return to your
command line.

Let's see what's inside our `joke.txt` file now.

```
$ cat joke.txt
```

There's our joke!

```
A man walks into a bar. The other one ducks.
```

We should probably make a folder called `funny_things` to put this joke in.

```
$ mkdir funny_things
```

> The `mkdir` command is used to create the specified folder. If the specified
> folder already exists, it will not be overwritten.
