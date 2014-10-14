**A Computer Program**



#### Variables

A lot of the times, after we calculate a value (whether it be a number or a
string), we want to save it somewhere so we can use it at later points in our
program. Let's look at the following example.

Create a file called `age.rb` and type into it the following Ruby code.

```ruby
puts("My age in years is")
puts(50)

puts("My age in months is")
puts(50 * 12)

puts("My age in days is")
puts(50 * 365)
```

Run the program using the command line (`$ ruby age.rb`). You should see
something like this.

```
My age in years is
50
My age in months is
600
My age in days is
18250
```

This is program that prints out a person's age in years, in months, and in days.
Can you modify this program for someone who is 21 years old? How many places did
you have to modify your code? Three times (each `50` needs to be changed to a
`21`).

Wouldn't it be convenient if we could give the number `50` a name (like `age`),
so that we can use it in our subsequent calculations without having to type `50`
again and again? It turns out that most programming languages allow you to do
that using a **variable**. We can name our variable almost whatever we want!
Let's try it.

```ruby
age = 50

puts("My age in years is")
puts(age)

puts("My age in months is")
puts(age * 12)

puts("My age in days is")
puts(age * 365)
```

The first line of this program now reads `age = 50`. This is _assigning the value 50 to
a variable called age_.

> A variable is a reference to a value. The assignment operator `=` is used to set the
> value that a variable should refer to.

Now, in the subsequent lines of the program, wherever we use the variable `age`,
we really mean the number `50`. Run this program and verify that it produces the
same output as before. If we wanted to modify this program for a 21 year old, we
would only have to make one change to our program!

Once we set a variable to a value, can we change it later in the program? Yes!
This is why we call them variables! Let's add to our age program to see what
this means.

```ruby
age = 50

puts("My age in years is")
puts(age)

puts("My age in months is")
puts(age * 12)

puts("My age in days is")
puts(age * 365)

age = 21

puts("Your age in years is")
puts(age)

puts("Your age in months is")
puts(age * 12)

puts("Your age in days is")
puts(age * 365)
```

First, the variable `age` is set to `50`, and three messages are printed for a
fifty year old. Then, the variable `age` is set to `21`, and three more messages
are printed, this time for a twenty-one year old. The resulting messages printed
by your program should look something like this.

```
My age in years is
50
My age in months is
600
My age in days is
18250
Your age in years is
21
Your age in months is
252
Your age in days is
7665
```

Instead of setting these variables to hard-coded values, we can ask the user to
enter these values when they _run_ the program. We do this using a friend of
`puts()`, namely `gets()`. We can use `gets()` to capture the user's input as
follows.

```ruby
age = gets().chomp().to_i()

puts("My age in years is")
puts(age)

puts("My age in months is")
puts(age * 12)

puts("My age in days is")
puts(age * 365)

age = gets().chomp().to_i()

puts("Your age in years is")
puts(age)

puts("Your age in months is")
puts(age * 12)

puts("Your age in days is")
puts(age * 365)
```

Run the program now. When your computer encounters a line of code that involves
`gets()`, your program will wait for the user to enter text. The program will
let the user keep typing until they press `Return` (or `Enter`). Once the user
presses `Return`, every thing they typed up to that point (including a "newline
character", which represents the `Return` key) will be captured by `gets()`.

What is the extra `chomp()` for? It removes the last newline that is present in
the string that is captured by `gets()`.

What is the extra `to_i()` for? It turns out `gets()` always gives you back a
string, even if the user entered numbers. This is because those numbers are not
interpreted as a number data type, but as numeric characters. Hence, we need to
convert that string to a number data type using `to_i()`.

After the result of `gets()` gets "chomped" and "to_i'd", we will be left with a
number that is stored in the variable `age`, and our program will proceed as
before.

Run the program now. Try inputting different numbers when your computer pauses
to allow you to enter a value for age. Is your program now using your user
input?
