**A Computer Program**



#### Exercise - Loops

Read the wikipedia entry for the [fizzbuzz](http://www.wikipedia.org/wiki/Fizz_buzz) game. Focus on the play section. Remove the player aspect from the game and write a simple algorithm for implementing the game using Ruby. Think about what conditions you must check for in order to play fizzbuzz. Think about some of the different datatypes you've learned about so far that will be of use for this exercise.

Write a Ruby program called `fizzbuzz.rb`. In this program:

* Print a statement that asks the user to input a number that is at least 25 that will act as a limit for the fizzbuzz game
	* if the user input does not satisfy the condition, prompt the user a second time to enter a number
	* if the user input does satisfy the condition then store it in a variable
* Define a variable `counter` and set it equal to 1
* Define a while loop that will run until the counter reaches the limit specified by the user
* Within the while loop define a conditional statement that will implement your algorithm. For each condition that is satisfied the appropriate string should be printed, i.e.

```ruby
	1
	2
	'fizz'
	4
	'buzz'
```

Run your program and make sure you are getting the correct output. _Remember_ if your program gets stuck you can use `Ctrl-c` to stop your program from executing.

* Does the order in which you define the conditions within the while loop matter?
* Did you run into any problems with your while loop?
