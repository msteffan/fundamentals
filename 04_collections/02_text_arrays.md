**Collections**

---

#### Arrays

> An array is an ordered list of objects.

In other words, an array is a container for a list of things. Usually those
things are similar (like a list of favorite movies). Also, order is important.
The position of each object inside the array is what makes it unique.

Here's what an array looks like in Ruby.

```ruby
[65, 63, 70, 74]
```

Arrays are represent by putting objects inside square brackets `[]`. Each object
is separated from the ones around it with commas `,`. Ruby allows you to put
objects of different types in the same array (like `["red", 42, "gorilla",
false]`), but we generally use arrays to deal with similar objects, or objects
of the same type.

The array above is an array of lap times run by our friend Timmy. Create a file
called `laps.rb` and inside, save the above array into a variable called
`lap_times`, and print the value of that variable.

```ruby
puts("Timmy has run 4 laps")
lap_times = [65, 63, 70, 73]
puts(lap_times)
```

Run this program. Did it print out your array?

When manipulating an array, we care about a few things. We care about

* Inserting new elements into the array
* Finding (or reading) elements from the array
* Modifying elements in the array
* Removing elements from the array

**Insert and Remove**

There are a number of ways we can insert elements into and remove elements from an array. The
important characteristic to keep in mind is _what position_ in the array we want
to insert or remove the value, since position is what lends structure to this
data structure.

It is very common to add/remove elements to/from the end of an array. Let's
modify our program to explore how to do so.

Let's say that Timmy ran two more laps (laps 5 and 6)

```ruby
puts("Timmy has run 4 laps")
lap_times = [65, 63, 70, 73]
puts(lap_times)

puts("Timmy ran 2 more laps")
lap_times.push(71)
lap_times.push(69)
puts(lap_times)
```

Run your program and see what happens. Two more lap times have been added to
our array!

> `an_array.push(a_value)` will insert `a_value` as a new element at the end of the array

Turns out Timmy cut corners on his last lap, so that lap time doesn't count.
Let's remove it from the end of our array.

```ruby
puts("Timmy has run 4 laps")
lap_times = [65, 63, 70, 73]
puts(lap_times)

puts("Timmy ran 2 more laps")
lap_times.push(71)
lap_times.push(69)
puts(lap_times)

puts("Timmy's last lap didn't count")
lap_times.pop()
puts(lap_times)
```

Run this program, and observe that the last object in the array has been removed

> `an_array.pop()` will remove and return the last object in an array

Note that we said "remove and return". Instead of just `lap_times.pop()`, you could have said `last_time = lap_times.pop()`. The last element in `lap_times` would be removed, but you would now be able to access it by referring to the `last_time` variable.

**Find/Read**

We can read, find, and access elements inside an array by referring to their
position in the array. In other words, arrays are capable of answering
questions like "What's the 4th object in you right now?".

One important thing to note about arrays in Ruby is that we start counting
positions **from 0**. In other words, the first element in an array has a
position (or index) of 0. The second element has an index of 1. The third has
an index of 2, and so on. Zero-based counting is standard across most programming languages.

Given an index, we can access the element at that index by using the following
notation.

```ruby
an_array[0]
an_array[1]
```

Using the square brackets with an index inside, right next to an array is
how we ask the array the question "what object do you have at position `index`?"

We can then save what we find in a variable like so.

```ruby
first_object = an_array[0]
second_object = an_array[1]
```

Let's find out some information about particular laps that Timmy ran.

```ruby
puts("Timmy has run 4 laps")
lap_times = [65, 63, 70, 73]
puts(lap_times)

puts("Timmy ran 2 more laps")
lap_times.push(71)
lap_times.push(69)
puts(lap_times)

puts("Timmy's last lap didn't count")
lap_times.pop()
puts(lap_times)

first_lap = lap_times[0]
fourth_lap = lap_times[3]

puts("Timmy's first lap time was:")
puts(first_lap)

puts("Timmy's fourth lap time was:")
puts(fourth_lap)
```

**Modify**

We can use the same technique to modify certain objects in an array. It turns
out that Timmy's second lap was actually 61 seconds. Let's make that change.

```ruby
puts("Timmy has run 4 laps")
lap_times = [65, 63, 70, 73]
puts(lap_times)

puts("Timmy ran 2 more laps")
lap_times.push(71)
lap_times.push(69)
puts(lap_times)

puts("Timmy's last lap didn't count")
lap_times.pop()
puts(lap_times)

first_lap = lap_times[0]
fourth_lap = lap_times[3]

puts("Timmy's first lap time was:")
puts(first_lap)

puts("Timmy's fourth lap time was:")
puts(fourth_lap)

puts("Fixing Timmy's second lap to 61 seconds")
lap_times[1] = 61
puts(lap_times)
```

Arrays in Ruby have some other very useful abilities we can use to get
information about them. Add the following lines of code to the end of
`lap_times.rb` and observe what they do.

```ruby
puts("What does first do?")
puts(lap_times.first())
puts("What does last do?")
puts(lap_times.last())
puts("What does count do?")
puts(lap_times.count())
```
