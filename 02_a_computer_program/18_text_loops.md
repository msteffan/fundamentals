**A Computer Program**



#### Loops

Using `if` statements, we can execute a section of code once if a certain
condition is met. Sometimes, we need to execute the same section of code
multiple times. For example, if we wanted to write a computer program to print
the lyrics to "99 bottles of beer on the wall", we wouldn't write 99 stanzas
worth of code. We would write the code for one stanza, and have our computer
repeat that code 99 times.

To achieve this functionality programmatically, make use of loops. In this
example, we will use a `while` loop. A while loop looks similar to our `if`
statement.

```ruby
while CONDITION
  # Do something
end
```

The major difference is that

> A `while` loop will repeat the section of code inside it until its condition
> is false.

Let's use a `while` to print a countdown starting from 10 and ending with
"Happy New Year!". Create a file called `happy_new_year.rb` and add the
following code to it.

```ruby
seconds_left = 10

while seconds_left > 0
  puts(seconds_left)
  seconds = seconds - 1
end

puts("Happy New Year!")
```

The code inside the `while` loop perfors the action of printing the current
number and then reducing the number by 1. We want to run the code inside the
`while` loop repetitively until the condition `seconds_left > 0` becomes false,
or in other words, as long as there are more than 0 seconds left.

Run your program. What output do you see?

```
10
9
8
7
6
5
4
3
2
1
Happy New Year!
```

It is very important to ensure that the condition that we pass to our `while`
loop (in this case, `seconds_left < 0`) will eventually become `false`. In our
example, the code inside our `while` loop reduced `seconds_left` by 1 with every
iteration, and eventually `seconds_left` was no longer greater than zero. If we
forget to ensure that our loop will end at some point, we would be stuck in an
infinite loop, and your computer might explode! Well, maybe your computer won't
explode, but you _will_ be stuck in an infinite loop.

> If your program is stuck due to an infinite loop (or any other reason), you
> can force your program to stop execution using the keyboard command `Ctrl-c`
