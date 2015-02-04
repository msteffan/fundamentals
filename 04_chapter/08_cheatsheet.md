**WDI Fundamentals Unit 4**

---

# Control Flow Cheat Sheet

Here are some notes on what's been covered in this chapter; feel free to copy this and extend it to make your own cheatsheet.

## Conditionals
### Ternary Operator
* The ternary operator takes in a condition; depending on whether that condition is is truthy or falsey, the operator will evaluate to one of two specified values.

  e.g. `(x > 10)? "Greater than 10." : "Less than 10.";`

* It can also be used inside larger expressions.

  e.g. "Today is " + ((temp > 70)? "" : "not") + " hot."

### `if...else` statement syntax

```javascript
if CONDITION_1
  # Code to be executed if CONDITION_1 is true
elsif CONDITION_2
  # Code to be executed if CONDITION_1 is false and CONDITION_2 is true
elsif CONDITION_3
  # Code to be executed if CONDITION_1 and CONDITION_2 are false, and CONDITION_3 is true
else
  # Code to be executed if CONDITION_1, CONDITION_2, and CONDITION_3 are false
end
```


* With `else if`, each additional condition will only be checked if all of the prior conditions have failed.

### `switch` statement syntax

```javascript
switch (expression)
{
case LABEL1:
  # Code to be executed if expression = LABEL1
  break
case LABEL2:
  # Code to be executed if expression = LABEL2
  break
default:
  # Code to be executed if expression is different from both LABEL1 and LABEL2
}
```

## Loops
* Loops are used to tell our programs to take repeated action.

### `while` Loops
* `while` loops can run indefinitely, so long as the condition remains true.
* The loop's condition is re-evaluated each time the block finishes running.

### `for` Loops
* A 'for' loop will generally run a fixed number of times, not indefinitely.
* The three paramters for a `for` loop, in order, are (1) an initialization, (2) a condition, and (3) a final expression.

[Let's put this into practice - here comes some more 'Rock Paper Scissors'!](09_assessment.md)
