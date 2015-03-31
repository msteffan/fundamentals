**WDI Fundamentals Unit 4**

---

# Control Flow Cheat Sheet

Here are some notes on what's been covered in this chapter; feel free to copy this and extend it to make your own cheatsheet.

## Conditionals
### Ternary Operator
* The ternary operator takes in a condition; depending on whether that condition is is truthy or falsey, the operator will evaluate to one of two specified values.

  e.g. `(x > 10)? 'Greater than 10.' : 'Less than 10.';`

* It can also be used inside larger expressions.

  e.g. `'Today is ' + ((temp > 70)? '' : 'not') + ' hot.';`

### `if...else` statement syntax

```javascript
if (condition1) {
  // Code to be executed if condition1 is true
} else if (condition2) {
  // Code to be executed if condition1 is false and condition2 is true
} else if (condition3) {
  // Code to be executed if condition1 and condition2 are false, and condition3 is true
} else {
  // Code to be executed if condition1, condition2, and condition3 are false
}
```


* With `else if`, each additional condition will only be checked if all of the prior conditions have failed.

### `switch` statement syntax

```javascript
switch (expression) {
    case value1:
      // Code to be executed if expression === value1
      break;
    case value2:
      // Code to be executed if expression === value2
      break;
    default:
      // Code to be executed if expression is different from both value1 and value2
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
