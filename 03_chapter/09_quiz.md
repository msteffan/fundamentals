**WDI Fundamentals Unit 3**

---

What does this statement evaluate to?*
- [ ] true
- [ ] false
- [ ] null
- [ ] undefined

> Not quite.
> The statement "10 > 9 > 8 === true;"  would evaluate to false.
> Here's why:
> According to JavaScript's order of operations, the line should be evaluated as: ((10>9)>8)
> Which evaluates to: (true > 8)
> Operators convert booleans to numbers, so this evaluates to: (1 > 8)
> Which is false.

Evaluate the last statement:*
HINT: what is the value of "x === x;"?
- [ ] true
- [ ] false
- [ ] null
- [ ] undefined

> Not quite.
> The statement "x === x"  would evaluate to true, because the variable does exist.
> The variable "x" alone would evaluate to null, as it exists but has not been assigned a value.

Again, evaluate the last statement:*
HINT: what is the value of "y === y"?
var x;
x === x;
y === y;

- [ ] true
- [ ] false
- [ ] null
- [ ] undefined

> Not quite. If you were to run this code in the console, JavaScript's response
would be ""ReferenceError: y is not defined".  JavaScript has no idea what "y"
is and would not be able to evaluate the statement.  So, the statement is
undefined.

What is the value of the variable "a"?*

var a = (null == false);
var b = (null == null);
var c = (undefined == null);
var d = (false == "");
var e = (false === 0);

- [ ] true
- [ ] false

> Not quite.
> While "null" has an inherently false value (it is "falsy"), it is not equivalent to anything except itself or the "undefined" value.

What is the value of the variable "c"?*

var a = (null == false);
var b = (null == null);
var c = (undefined == null);
var d = (false == "");
var e = (false === 0);

- [ ] true
- [ ] false

> Not quite.
> While "undefined" and "null" are falsy values, it is true that "undefined == null".

What is the value of  d || e ?*
HINT: first evaluate "d" and "e"

var a = (null == false);
var b = (null == null);
var c = (undefined == null);
var d = (false == "");
var e = (false === 0);

- [ ] true
- [ ] false

> Not quite.
> The first variable, "d" is true, because an empty string has a falsy value.  You don't even need to evaluate the second variable, because the || (OR) operator will return true if at least one of the inputs is true.

---

[Here's another exercise for you](10_exercise.md) - give it a shot.
