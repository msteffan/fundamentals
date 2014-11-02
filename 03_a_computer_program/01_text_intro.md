**WDI Fundamentals Chapter 2**

# A Computer Program

## Learning Objectives

* List different data types in a programming language
* Perform arithmetic operations on data to produce new values
* Store values in variables to subsequently use in expressions
* Perform comparison operations on data to produce boolean values
* Use conditional statements to control the flow of program execution
* Use loops to programmatically repeat a section of code
* Locate and correct errors in a program based on standard error messages

**Feel free to create a dedicated folder (such as `ch_3`) inside the
`fundamentals` folder, in which you can store any files that you are
asked to create in this chapter.**

## Outline

#### Fundamentals

> The great thing about computers is that they do exactly what you tell them to
> do. The terrible thing about computers is that they do _exactly_ what you tell
> them to do.

We use computers to perform tasks that would be time consuming for us to perform
manually. A great example of such a task is calculating your taxes. Computers
can crunch numbers extremely fast. The very computer you are on right now can
perform around two billion arithmetic operations every second! The average human
being can probably do one or two every second.

Another reason that we get computers to do our dirty work is that they are very
accurate in their operations. If you ask a computer to do a million math
problems, chances that it will make a mistake are virtually zero. A human, on
other hand, would be prone to (rightfully-named) human error.

Hold on. If that's the case, if computers are super fast and super accurate, why
don't we use them to accomplish every single thing in the world? Why do there
still exist jobs that have not been automated with computers?

Though they are fast and accurate, computers need to be told how to do their job
with very explicit instructions. We call a set of these instructions a program.

If you wanted your friend to make a peanut butter and jelly sandwich, you might
say to them "Can you make me a PB&J?". If you wanted a computer to make you a
PB&J, your instructions would have to be much more detailed.

```
Locate the bread
Locate the peanut butter
Locate the jelly
Locate a plate
Locate a knife
Open the bread's plastic cover
Take out two slices of bread
Place those two slices of bread on the plate side by side
Twist off lid of peanut butter
Place lid on counter
Pick up knife
Scoop one tablespoon of peanut butter
Deposit peanut butter on the first slice of bread on plate
And so on...
```

This is a taste of the level of explicitness required to write a program.
A computer can only understand very basic instructions (like 'locate the bread',
or 'add two numbers together'). It is up to us as developers to be able to
assemble a set of these simple instructions into a complicated action.

> A set of very low-level steps to be executed exactly and in the specified
> order, as in the PB&J example, is called an *algorithm*. An implementation of
> an algorithm to be executed by a computer is called a *program*.
