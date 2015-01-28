**WDI Fundamentals Unit 4 - Flow Control**

---

# Conditionals

## The Ternary Operator - ` __ ? __ : __ `

The simplest type of 'conditional' behavior found in JavaScript is an operator called a 'ternary' operator. Its syntax is as follows:

  `some_expression ? truthy_value : falsey_value`

The ternary operator will evaluate to one of the two values on the right, depending on whether the expression on the left is truthy or falsey. Here's an example of a ternary operator with some actual values plugged in.

  `true? 1 : 2`

Since `true` is (obviously) truthy, this means that the *entire expression* will evaluate to the specified value - in this case, 1.

Naturally, an expression with a ternary operator can also be incorporated into larger expressions. For example, `((x > 5)? 10 : 20)*10` will evaluate to 100 if `x` is greater than 5, or 200 if `x` is *not* greater than 5.

### Test Yourself
Suppose that we have two variables, `x` and `y`. `x` is (at the moment) equal to 10, while `y` is equal to 20. What values would the following expressions evaluate to? Check your answers in repl.it.
* (x%2 == 0)? "even" : "odd"
* (x > y)? 1 : 0
* (3)? 100 : -100
* ('')? "hello" : "goodbye"


## `if..else if...else` Statements

What if, rather than controlling how an expression evaluates, we wanted to use some truthy/falsey condition (hence the name 'conditionals') to optionally run one line of code vs another?

JavaScript has a tool to do just that, called `if`. An `if` statement will take in a condition and, if that condition is truthy, will run whatever code you specify. Here's an example of an `if` statement in action.
  ```javascript
  if (x > 10) {
    x += 10;
    y += 10;
  }
  ```
The condition is what's inside the parentheses; if that condition is truthy (and it is, in this case), the lines of code inside the curly braces (`{...}`) will be evaluated one by one.

Let's take a step back for a minute, and consider something that's closer to our own experience : a flow chart.

![XKCD Flow Chart]()
*<small>src: [http://xkcd.com/518/](http://xkcd.com/518/)</small>*

A flow chart is a visual diagram telling us how to behave, depending on some set of conditions. If we were to try to draw a flow chart to describe an `if` statement, we might come up with something like this:

![Flow Chart for `If` Statement]()

As you can see, a person making their way through this diagram would need to make a decision; depending on whether or not our condition is truthy, they would either enter the block of code or skip it over entirely.

`if` can actually be modified in several ways to change its behavior. For instance, adding an `else if` to our `if` statement allows us to specify a second condition to test; however, *this second condition will only be tested if the first condition fails*.

```javascript
  if (x > 10) {
    x += 10;
    y += 10;
  } else if (x > 5) {
    x += 5;
  }
```
<aside style="float: left;">![Flow Chart for `If...Else If` Statement]()</aside>

We can add as many `else if`s as we want - just keep tacking them on.

```javascript
  if (x > 10) {
    x += 10;
    y += 10;
  } else if (x > 5) {
    x += 5;
  } else if (x > 3) {
    x += 3;
  }
```
<aside style="float: left;">![Flow Chart for `If...Else If...Else If` Statement]()</aside>

However, if all of the conditions fail, nothing will happen. To specify behavior for this outcome, we must add an `else` to the end of our statement, like so.

```javascript
  if (x > 10) {
    x += 10;
    y += 10;
  } else if (x > 5) {
    x += 5;
  } else if (x > 3) {
    x += 3;
  } else {
    x += 1;
  }
```
<aside style="float: left;">![Flow Chart for `If...Else If...Else If...Else` Statement]()</aside>

Using `if...else if...else` statements allows us to write code that can behave very differently in different circumstances.

### Test Yourself
Consider following conditional statement:
```javascript
if (x > 5) {
  y = 50;
} else if (x < 5) {
  y = 33;
} else {
  y = 100;
}
```
* What value will be assigned to `y` if ...
  * x is 10?
  * x is 4?
* Under what circumstances will `y` be assigned a value of 100?

Try copying that whole statement into repl.it, and testing out different values for `x`. Were your answers correct?


## Switch Statement

As we've seen before, we can choose which condition will be executed using `if...else...if`; however, if we have a lot of conditions, the code become a bit repetitive and hard to read. For example :

```javascript
// day of the week in a number, sunday is 0, saturday is 6
dayNumber = 1
if(dayNumber == 0){
  day = "Sunday";
} else if(dayNumber == 1){
  day = "Monday";
} else if(dayNumber == 2){
  day = "Tuesday";
} else if(dayNumber == 3){
  day = "Wednesday";
} else if(dayNumber == 4){
  day = "Thursday";
} else if(dayNumber == 5){
  day = "Friday";
} else if(dayNumber == 6){
  day = "Saturday";
} else {
  day = null;
  alert("wrong value for day");
}

```

What this code does, fundamentally, is pretty simple - it takes in a number (representing a particular day of the week) and spits out a string containing the name of that day. However, this code is not easy to read, and a lot of code is repeated - for example, `} else if(dayNumber == X){` is repeated 7 times. What's more, if we ever want to change the name of our `dayNumber` variable, we'll need to swap it out every times it appears, which is a bit of a pain.

Enter the `switch` statement:
```
dayNumber = 1

switch (dayNumber) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
    break;
  default:
    day = null;
  alert("wrong value for day");
}
```
This code works exactly the same as our `if..else..if`, but although it's slightly longer (in terms of lines), it is significantly easier to read.

In a `switch` statement, the variable in parentheses (in this case, `dayNumber`) gets evaluated; if there is a `case` listed for the value that it evaluates to, the code between `case __:` and `break` will be executed. If there is no `case` that matches the value of the variable, the `default` will be executed (if it is specified - if not, the program will do nothing).

> Note: If there is no `break;` at the end of a `case`, the computer will not skip to the end, but will instead start  executing the *next* case's code (even if `case`'s value is different from the variable'), and will continue doing so until it eventually hits a `break;` statement. For this reason, `default` never needs a `break;` statement, because it's the last `case` in the `switch`.

Although the `switch` statement sometimes has some advantages over `if...else if... else`, it also has some major disadvantages. For instance, a `switch` statement will only work if you are testing the same variable (or expression) in every condition; if not, the `if...else if...else` is your only option. Also, depending on the circumstances, using `if...else if...else` might scan more naturally.

### Test Yourself
Consider the following `switch` statement.
```javascript
switch (2 * x) {
 case 2:
    y = 49;
    break;
 case 4:
    y = 37;
    break;
 case 6:
    y = 25;
    break;
 case 8:
    y = 13;
    break;
 default:
    y = 1;
}
```
What value will `y` be assigned when `x` is ...
* 1?
* 4?
* 0?
* "Hello"?

[Here's a short quiz on everything we've covered so far - do your best!](03_quiz.md)





