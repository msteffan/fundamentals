**WDI Fundamentals Unit 4 - Flow Control**

---

# Flow Control Cheat Sheet

Here are some notes on what's been covered in this chapter; feel free to copy this and extend it to make your own cheatsheet.

## Conditionals
### Ternary Operator
* The ternary operator takes in a condition; depending on whether that condition is is truthy or falsey, the operator will evaluate to one of two specified values.

  e.g. `(x > 10)? "Greater than 10." : "Less than 10.";`

* It can also be used inside larger expressions.

  e.g. "Today is " + ((temp > 70)? "" : "not") + " hot."

### `if...else if...else` Statements
* Used to run one of several blocks of code based on some condition (or a set of conditions).
* With `else if`, each additional condition will only be checked if all of the prior conditions have failed.
* `else` specifies what happens if all prior conditions fail.
* When a program runs through `if...else if...else if... else' statement, **only one of the blocks will be executed** at that time.

### `switch` Statements
* `switch` can take away some of the duplication from long `if...else if...else` statements.
* One limitation of `switch` is that it can only use cases that are different values of the same expression - it is less flexible than `if...else if...else`.

## Loops
* Loops are used to tell our programs to take repeated action.

### `while` Loops
* `while` loops can run indefinitely, so long as the condition remains true.
* The loop's condition is re-evaluated each time the block finishes running.

### `for` Loops
* A 'for' loop will generally run a fixed number of times, not indefinitely.
* The three paramters for a `for` loop, in order, are (1) an initialization, (2) a condition, and (3) a final expression.

