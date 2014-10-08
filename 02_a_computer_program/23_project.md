**A Computer Program**

---

# A Computer Program - Exercise

## Objectives

* Practice with variables and data types
* Practice with user input and output
* Practice with control flow using `if` statements

It's time to revisit `project_todo`. Navigate to your `project_todo` folder and
open up `main.rb`. Remove any code that is in there presently, and let's get
started.

#### Phase 1

Write code to ensure your program does the following things.

* Print a message welcoming the user to your application (eg. "Welcome to
Project Todo")
* Print a series of messages to form a menu, that looks like this

```
Menu
----
1. View my todos
2. Add a todo
3. Complete a todo
4. Exit
Enter your choice:
```

* Capture the user's input in a variable called `user_input`. Make sure to
  convert this to a number.
* Print a message showing what the user entered. For example,

```
The user entered
3
```

Run your program and verify that it displays the right messages, pauses, and
allows the user to enter an input. After the user presses the `Return` key, the
program should print a message saying what the user entered.

#### Phase 2

After printing a message saying what the user entered, make use of `if-elsif`
statements to print different messages depending on what the user inputted.

* `1` - "Under construction. You will be able to view your todos soon!"
* `2` - "Under construction. You will be able to add todos soon!"
* `3` - "Under construction. You will be able to complete todos soon!"
* `4` - "Thank you for using Project Todo. Have a nice day."

#### Phase 3

Modify your program so that all the code relating to displaying the menu and
handling the user input (so, everything except the first welcome message) is
wrapped inside a `while` loop. What should the condition for the `while` loop
be? `true`!

```ruby
puts("Welcome to Project Todo!")
while true
  # Display the menu
  # Gather user input
  # If-else statements to handle user input
end
```

"Wait a second! Won't this loop run forever?" Yes it will, since the condition
(`true`) will always be true! However, there is another way to "break out" of
a `while` loop, and that is utilizing the keyword `break`.

If the user enters `4`, not only should we display the message for option 4, we
should also use `break` to exit the loop.

```ruby
puts("Thank you for using Project Todo. Have a nice day.")
break
```

Run your program now. At this point, after selecting either menu option 1, 2, or
3, the appropriate message will be displayed, the menu will be re-displayed, and
you will be prompted for another input. Only selecting option 4 will execute the
`break` and hence will break out of the loop and terminate your program. Take
your new app for a spin!
