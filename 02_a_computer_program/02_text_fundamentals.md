**A Computer Program**



#### Fundamentals

There are many different languages we can use to write computer programs.Let's
write our first program in Ruby!

First, create a file called `departure.rb` to begin our programming journey.
The `.rb` extension indicates that this file will contain some instructions
written in Ruby. Open up this file and type in the following.

```ruby
# Time for departure
24 / 8
4 * 5
10 - 6
1 + 2
```

Save and close this file.

Believe it or not, you've written a program. The first line of this program is a
comment. Comments are ignored by your computer when you run programs. They are
used to explain to other programmers (including your future self) what your code
is doing. In Ruby, any line beginning with a `#` will be interpreted by your
computer as a comment.

The next four lines of your program work with a particular type of data, namely
numbers. Ruby programs have other types of data that we can use as well. We'll
explore the others soon.

At this point, we've written some instructions for our computer to run, but we
haven't yet told our computer to run these instructions. Let's do that by
opening up our command line, navigating to the folder where we have saved our
program, and running the following command.

```
$ ruby departure.rb
```

Did anything happen? Probably not. Why? Well, we told our computer to perform
those four arithmetic operations, one after the other. Trust that your computer
did indeed perform those three calculations. However, we didn't tell our
computer to display the answers to us when it was finished calculating! (They do
_exactly_ what you tell them to, nothing more, nothing less).

Ok, let's modify our program so that the answers are printed so we can see them.

```ruby
# Time for departure
puts(1 + 2)
puts(10 - 6)
puts(4 * 5)
puts(24 / 8)
```

`puts()` is a nice tool that Ruby gives us that can print things out for us to
see. We simply put what we want to be printed inside the parentheses. In
technical terms, `puts()` is a method, but more on that later. For now, let's
simply use it when we want something to be displayed on the screen to see.

Let's run our program again using the same command (`$ ruby departure.rb`).
There we go!

```
3
4
20
3
```

Our computer executed the instructions that we gave it one after the other from
top to bottom. Let's modify our program to utilize another data type, strings.

```ruby
# Time for departure
puts(1 + 2)
puts(10 - 6)
puts(4 * 5)
puts(24 / 8)
puts("I am a string.")
puts("So am I!")
puts("You can add " + "strings together!")
```

A string in programming is a value that represents a set of characters. These
characters can be letters, punctuation, special characters (`@`,`#`, `$`, etc.),
or even numeric characters. In Ruby, we represent a string by putting it between
single or double quotes. This way, when our computer reads through our program,
it will understand that `I am a string` is not code to be executed, but a set of
characters.
