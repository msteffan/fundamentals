**Collections**



#### Iteration

When working with a set of data like an array, we often need to step through
one object at a time and perform some action with each object. This could be
necessary to do something as simple as printing each element of the array like
so.

```
** 65 **
** 61 **
** 70 **
** 73 **
** 71 **
```

We call this process of stepping through an array one object at a time
**iteration**.

> Iteration is the process of stepping through the elements of a data structure
> one element at a time, usually to perform an action on or with each element
> of the data structure.

This certainly seems like we want to repeat a secion of code programmatically
until a certain condition. Sounds like a job for our `while` loop!

Let's write a program called `oddball.rb`. Fill in the following code into the
program to start.

```ruby
numbers = [6, 2, 3, 15, 4, 8, 7, 3]
```

The purpose of this program is to iterate through the `numbers` array, and print
a message for each element. If the element is odd, we will print `ODD`, and if
the element is even, we will print `EVEN`.

First, let's simply print out each number, to make sure that our `while` loop
can properly iterate over the array. Here are some things to keep in mind about
this `while` loop.

* We need a variable to keep track of which index of the array we are at at any
  given time
* This variable needs to start from zero (remember, indices of an array start
  counting from 0)
* This variable needs to increment (increase by 1) every time we print a number
  to take us to the next element of the array
* We need to stop looping when we've reached the end of our array.
* If an array has 5 elements, the last element has a position of 4

Let's write some more code in our program.

```ruby
numbers = [6, 2, 3, 15, 4, 8, 7, 3]

# This variable will keep track of our position in the array
index = 0

# We need to keep going as long as our index is
# less than the number of elements in our array
while index < numbers.count()
  # Grab the element at the position 'index'
  current_number = numbers[index]

  # Print that number
  puts(current_number)

  # Move to the next position
  index = index + 1
end
```

Run your program and watch it print out each number of the array. Now that we've
gotten the trivial stuff out of the way, let's implement oddball. Instead of
simply printing each number, we need to print either `ODD` or `EVEN` based on
what the number is. Let's modify our code to do that.

```ruby
numbers = [6, 2, 3, 15, 4, 8, 7, 3]

# This variable will keep track of our position in the array
index = 0

# We need to keep going as long as our index is
# less than the number of elements in our array
while index < numbers.count()
  # Grab the element at the position 'index'
  current_number = numbers[index]

  # Print the right message based on the number
  if current_number.odd?()
    puts("ODD")
  else
    puts("EVEN")
  end

  # Move to the next position
  index = index + 1
end
```

What is `.odd?()`? Just like our arrays had special abilities like `.first()`,
numbers in Ruby also have special abilities. One of those abilities is `.odd?()`,
which produces `true` if the number is odd, and `false` if the number is even.

Run your program and observe its output. Success!
