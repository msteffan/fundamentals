**WDI Fundamentals Unit 1**

---

##Moving and Removing Things

Before we start the next section, let's navigate to our home folder.

```
$ cd ~
```

We made a folder for our joke called `funny_things` (you can check that it is
there by running the `ls` command). How do we move our `joke.txt` file into this
folder? If we were using Finder, we might use our mouse to drag and drop
`joke.txt` into `funny_things`. Can we achieve the same action with our command
line? You guessed it, yes we can.

```
$ mv joke.txt funny_things/
```

Voila! Our hilarious joke has been moved, rightfully, into the `funny_things`
folder.

> The `mv` command moves the specified files or folders to the specified
> destination.

This is the first time we've used a command that needed two pieces of
information from us, or two arguments. The first argument is "what to move", and
the second argument is "where to move it to".

Let's navigate to our `funny_things` folder and check its contents to
make sure that this worked.

```
$ cd funny_things
$ ls
```

Copying files is similar to moving them. Let's make a copy of our joke.

```
$ cp joke.txt joke2.txt
```

> The `cp` command is used to copy the specified files or folders to the
> specified location.

After running this command, we have created a copy of `joke.txt` called `joke2.txt` in the same folder. Notice how in this case, the second argument was a filename, and not a folder
name. It turns out that the `mv` and `cp` commands are quite smart. When moving or copying
a file, if the second argument is a **folder**, the specified file is moved or
copied to that folder. If the second argument is a **filename**, the file in the first argument
is moved or copied to a file with the filename specified in the second argument. Hence, when we copied
our joke, our file `joke.txt` was copied to another file called `joke2.txt`.

Perhaps we should make another folder inside `funny_things` called `jokes`, and
put our joke in there. After all, we could have funny jokes, funny pictures, and much
more. In order to achieve this, we're going to follow a series of long-winded
steps so we may familiarize ourselves with some more useful commands.

First, we're going to get rid of our duplicate joke file.

```
$ rm joke2.txt
```

> The `rm` command, which stands for remove, deletes the specified files
> from your computer. `rmdir` (remove directory), deletes specified folders
> if they are empty. **Be careful with these commands!** These actions
> do not move files to your Trash, where you can recover them. These
> actions **permanently remove** the specified files and folders. They are
> **irrecoverable**.

Now that all the copycats are out of the way for good, let's make a `jokes`
folder and put our joke inside.

```
$ mkdir jokes
$ mv joke.txt jokes/joke.txt
```

If you are trying to copy or remove folders, and not files, we need to add "an
option" to our command. Options are extra settings that we want to apply to our
commands. Options to commands are always of the format `--word` or `-letter`.
For example, let's try to copy our jokes folder.

```
$ cp -r jokes copy_of_jokes
```

> The `-r` option stands for "recursive", and must be applied to the `cp`
> command when copying folders.

This is because not only do we want to copy the folder, we also want to
recursively copy the contents of that folder, and the contents of any folders
inside as well.

The same principle applies when removing a folder with files. The `rm -r` command will remove all of a folder's content as well as the folder itself.

```
$ rm -r copy_of_jokes
```

Note that the `mv` command does not need a `-r` option to move folders.

