**A Computer Program**

---

#### Exercise - Logical Operators

Write a Ruby program called `hot_or_cold.rb`. In this program:

* Assign any value to a variable called `current_temp`
* Print out a statement that asks the user if this is their house, and instruct them to type '1' if yes and '0' if not.
* Use the `gets()` method to accept and store the user's input in a variable called `my_house_input`
* Define a conditional statement that performs the following actions:
  * If `my_house_input` = 1, set `my_house` = true
  * If `my_house_input` = 0, set `my_house` = false

* Print out a statement that asks if the user wants to 'increase' or 'decrease' the temperature.
* Use the `gets()` method to accept and store the user's input in a variable called `temp_direction`

* Print out a statement that asks the user by how much they want to increase the temperature
* Use the `gets()` method to accept and store the user's input in a variable called `temp_delta`

* Define a conditional statement that uses logical operators to perform the following actions based on the user's input:

  * If this is the user's house and they want to increase the current temperature,
    * Set a variable `new_temperature` equal to the current temperature plus `temp_delta`
    * Print the statement 'Heating up the house to `new_temperature`'

  * If this is the user's house and they want to decrease the current temperature,
    * Set a variable `new_temperature` equal to the current temperature minus `temp_delta`
    * Print the statement 'Cooling down the house to `new_temperature`'

  * Otherwise, print the statement 'Sorry, this is not your house.'
