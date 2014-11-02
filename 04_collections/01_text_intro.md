**WDI Fundamentals Chapter 3**

# Collections
![Collections](../images/icon_collections.png "Collections")


## Learning Objectives

* Explain the need for data structures to manage data
* List two common data structures commonly used in programming
* Differentiate between hashes and arrays
* Add and remove elements from hashes and arrays
* Access and modify elements in hashes and arrays
* Iterate over the elements of an array

**Feel free to create a dedicated folder (such as `ch_4`) inside the
`fundamentals` folder, in which you can store any files that you are
asked to create in this chapter.**

## Outline

#### What's the problem?

As programs grow in complexity, so does the data that they work with. It quickly
becomes necessary to make use of some more programming tools to manage this data
in a sensible and efficient way. Before we dive into these new tools right away,
it is important to feel the need for them, so that you may develop a deep
understanding of the problem that they solve. Let's do this through an example.

We decide that we want to write a program that will allow us to keep track of
our top three favorite movies.

Create a file called `movies.rb`. In it, use `gets()` to prompt the user for input
three times, and store the three movies that the user entered into variables
`movie_1`, `movie_2`, and `movie_3`. After the user has entered three movies,
display a message stating what the user's favorite movies are.

Your code probably looks something like this.

```ruby
puts("What's your number 1 favorite movie?")
movie_1 = gets().chomp()
puts("What's your number 2 favorite movie?")
movie_2 = gets().chomp()
puts("What's your number 3 favorite movie?")
movie_3 = gets().chomp()

puts("Awesome.")
puts("Your number 1 favorite movie is " + movie_1)
puts("Your number 2 favorite movie is " + movie_2)
puts("Your number 3 favorite movie is " + movie_3)
puts("I think you have good taste in movies. Goodbye.")
```

Run your program. Enter your top three favorite movies. Great!

What if we decided that instead of our top three movies, we wanted to keep track
of our top ten movies? Modify your code to do this.

```ruby
puts("What's your number 1 favorite movie?")
movie_1 = gets().chomp()
puts("What's your number 2 favorite movie?")
movie_2 = gets().chomp()
puts("What's your number 3 favorite movie?")
movie_3 = gets().chomp()
puts("What's your number 4 favorite movie?")
movie_4 = gets().chomp()
puts("What's your number 5 favorite movie?")
movie_5 = gets().chomp()
puts("What's your number 6 favorite movie?")
movie_6 = gets().chomp()
puts("What's your number 7 favorite movie?")
movie_7 = gets().chomp()
puts("What's your number 8 favorite movie?")
movie_8 = gets().chomp()
puts("What's your number 9 favorite movie?")
movie_9 = gets().chomp()
puts("What's your number 10 favorite movie?")
movie_10 = gets().chomp()

puts("Awesome.")
puts("Your number 1 favorite movie is " + movie_1)
puts("Your number 2 favorite movie is " + movie_2)
puts("Your number 3 favorite movie is " + movie_3)
puts("Your number 4 favorite movie is " + movie_4)
puts("Your number 5 favorite movie is " + movie_5)
puts("Your number 6 favorite movie is " + movie_6)
puts("Your number 7 favorite movie is " + movie_7)
puts("Your number 8 favorite movie is " + movie_8)
puts("Your number 9 favorite movie is " + movie_9)
puts("Your number 10 favorite movie is " + movie_10)
puts("I think you have good taste in movies. Goodbye.")
```

That was a little tiring. Ok, run your program and make sure it still works.

What if we decided to keep track of hundred movies? Do we really have to go
write about two hundred lines of code to do this? There are two bad things about
our approach to solving this problem.

1. The more movies we want to keep track of, the more tedious it is to write
   the code to do so (our code is growing even though our program is not
   growing in complexity)
2. This is a subtler point, but if we want to keep track of a different number
   of movies, we are forced to **change our code**. Our code is not flexible
   enough to handle different numbers of movies "on the fly".

These are the problems we are aiming to solve. We can solve them with an array!
