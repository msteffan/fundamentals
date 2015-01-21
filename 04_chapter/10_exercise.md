**A Computer Program**

---

#### Comparison operators and conditional statements

We've seen that we can perform arithmetic operations on numbers. We can also
perform comparison operations on them. Using these operations, we can determine
whether a number is bigger, smaller, or equal to another number. We'll see why
this is useful in little bit. Before that, let's explore comparison operators.

Create a Ruby file called `scales.rb` and enter the following code into it.

```ruby
puts("Is 12 greater than 5?")
puts(12 > 5)

puts("Is 12 less than 5?")
puts(12 < 5)

puts("Is 12 equal to 5?")
puts(12 == 5)
```

Run this program and see what happens.

```
Is 12 greater than 5?
true
Is 12 less than 5?
false
Is 12 equal to 5?
false
```

What are these new values that we're encountering? They are `true` and `false`,
and they are another type of data in Ruby called **booleans**. Boolean values
are great at representing whether something is true or not. You could use a
boolean value to keep track of whether the light in your room is off or on. The
value `true` could indicate on, and the value `false` could indicate off.

> The comparison operators we just used produce boolean values to indicate whether the
> comparison is correct or not.
>
> * Greater than (`>`) produces `true` if the number on the left is bigger than the number
>   on the right, and false in all other cases
> * Less than (`<`) produces `true` if the number on the left is smaller than the number
>   on the right, and false in all other cases
> * Equal to (`==`) produces `true` if both number are the same, and false in all other
>   cases
>
> In addition to these, there exist other comparison operators that perform different
> comparisons.
>
> * Greater than or equal to (`>=`) produces `true` if the number on the left is either
>   bigger than the number on the right, or the same as the number on the right.
> * Less than or equal to (`<=`) produces `true` if the number on the left is either smaller
>   than the number on the right, or the same as the number on the right.
> * Not equal to (`!=`) produces `true` when the two numbers are not equal, and `false` if
>   they are equal.

So far, the programs we have written will execute every line of code from top to
bottom. In other words, they will do exactly the same thing every time you run
them. Often it is useful to have our program decide whether to perform one
action or another, depending on the present conditions in the program. Consider
a relatable analogy referring to our PB&J.

```
Locate the bread
If you found the bread, proceed to locate the jam
If you didn't find the bread, proceed to the store to buy bread
```

Here, when we are writing these instructions for our computer (or friend) to
make us a sandwich, we do not know whether they will be able to locate bread or
not. Hence, our instructions need to involve deciding what to do depending on
whether or not we have bread.

Similarly in programming, we commonly want to decide whether to perform a set of
actions based on a certain condition. We can do this with the use of an `if`
statement.

Create a Ruby program called `bouncer.rb` and enter the following code into it.

```ruby
puts("Let me check your ID.")

age = 18

if age < 21
  puts("Come back when you are older!");
end
```

Did this program tell you to come back when you are older when you ran it? It
probably did! This is because the condition `age < 21` produced the value
`true`, and an `if` statement will perform the actions inside it if its
condition evaluated to `true`. The `end` is important because it denotes just
how many lines of code lie 'inside' the `if` statement. Change the value of the
`age` variable to 25 and see if the bouncer rejects you now.

Perhaps our bouncer is polite, and offers a friendly greeting if you are indeed
old enough to enter. There is a convenient way to perform an alternative set of
actions if the condition evaluates to `false`, namely, an `else` statement.
Let's modify our program to look like this.

```ruby
puts("Let me check your ID.")

age = 18

if age < 21
  puts("Come back when you are older!");
else
  puts("Thank you. Come on in.")
end
```

Run the program. Was the bouncer rude? Modify the value of the `age` variable to
25 and run the program again. Did the bouncer offer a friendly greeting this
time around? Excellent!

In this example, we manually changed the value of the variable `age`. In a real
scenario, that number might come from a database, or what the user entered in a
form.

If we want to choose between more than two actions to perform based on certain
conditions, we can use an `elsif` statement. Let's make our bouncer a little
more aware of the people coming in.

```ruby
age = 18

if age < 21
  puts("Come back when you are older!");
elsif age < 50
  puts("Thank you. Come on in.")
else
  puts("No need to card you, right this way!")
end
```

This code will execute a different action depending on whether the age is less
than 21, between 21 and 50, or 50 and above. This code almost reads like
English. "If age is less than 21, do the first thing. Else, if the age is less
than 50, do the second thing. Else, do the third thing."
