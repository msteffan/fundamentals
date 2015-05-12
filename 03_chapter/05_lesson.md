**WDI Fundamentals Unit 3**

---

# Expressions with Variables

One major calculator function that we haven't mentioned so far is **memory**. Many calculators have buttons that can be used to store the results of calculations in memory for later use. JavaScript's answer to this is **variables**.

Suppose that we wanted to save the result of our expression, `(99 * 746) - (837 * 23)`, and then multiply the whole thing by `2` later. We could store our first result in a variable `x` using `=` (the 'assignment' operator) as follows:

`var x = (99 * 746) - (837 * 23);`

> **HINT**  The <b>keyword</b> `var` stands for `variable` and is used to *declare* a variable the first time we use it. A variable *can* be declared without using the keyword `var`, but this has major implications on where that variable is stored and what code can access it. You'll learn more about this when you cover the concept of <b>scope</b>. For now, always declare your variables using `var`.

When we want to then use this result, we simply subsitute `x` for wherever our original expression might have gone; for instance, we could write `x * 2;` and this expression would evaluate to double whatever value was stored in `x`.

To figure out how to evaluate an expression containing variables, we simply draw a tree, as before. The only difference is that `x` (or whatever other variable we might be using) evaluates to whatever value it's storing at the time.

### Test Yourself
Assume that `x` is equal to 10. What values do the following expressions evaluate to? Check your answers in repl.it.

* `x + 20`
* `x * x`
* `3 * (x * x) - 2 * x + 5`

We can redefine our variable `x` as many times as we want. However, ***only the most recent value of `x` is retained*** - once `x` gets redefined, its original value is lost forever.

Suppose we ran the following lines of code in order, one by one.

```javascript
var x = 10;
x = 1;
x = 5;
x = 15;
2 * x;
```
What does that last expression evaluate to? Or, put differently, what is the most recent value of x (as of that line) multiplied by 2? If you guessed 30, then you're correct!

> **HINT** `=` is called the <b>assignment operator</b>. One interesting fact about it is that it actually returns a value after it's finished its "assignment" work. In particular, the `=` operator evaluates to whatever the expression to the right of the `=` evaluates to. In other words, the expression `x = 2` returns `2`.

Sometimes, we find variables on both sides of the `=`. Suppose we have two variables, `x` and `y`, as in the example below.

```javascript
var x = 5;
var y = 10;
x = y + 10;
```

What happens in that third line? For starters, everything to the right of the `=` must be evaluated before any kind of assignment can happen. `y + 10` evaluates to 20, so what we're left with is the expression `x = 20`. This assigns the value 20 to `x`, and the entire expression evaluates to 20.

Let's look at one more example using the same two variables, `x` and `y`.

```javascript
var x = 1;
var y = 10;
x = y * 2;
y = x + 1;
x = y + 1;
y = 2 * x;
```

Feeling dizzy? Don't worry, we'll step through this one together.

  __Line 1__: We declare a new variable `x` and assign it the value `1`.

  __Line 2__: We declare another new variable `y` and assign it the value 10.

  __Line 3__: As of this point in the code, `y` has a value of 10. We multiply that by 2, resulting in 20. We assign that resulting value to `x`.

  __Line 4__: `x` now has a value of 20, so `y` gets assigned a new value of 21 (`20 + 1`).

  __Line 5__: `y` was just changed to 21, so `x` becomes 22 (`21 + 1`).

  __Line 6__: `x` is now 22, so `y` becomes `2 * 22`, or 44.

One important thing to mention here is that **at no point is any lasting relationship established between x and y** (unlike how equations work in math). We are simply evaluating the expression on the right and assigning the result to the variable on the left.

### Test Yourself
Give these a try – see if you can predict the final values of `x`, `y`, and `z`. Check your answers in repl.it by copying the entire chunk of code into the editor window, running it, and then checking `x`,`y`, and `z` in the repl.it terminal.

##### Challenge \#1

```javascript
var x = 1;
var y = 2;
var z = 3;
x = y;
y = z;
z = x;
```

##### Challenge \#2

```javascript
var x = 1;
var y = 0;
var z = -1;
x = y + z;
y = z * x;
z = x - y;
x = y * y;
y = z * z;
z = z - 1;
```

Whoa! That last one's pretty weird - how can z be on both sides of the `=`? What do you think happens there?

The key is remembering how the `=` operator works - before it assigns anything to the variable on the left, *it first evaluates the expression on the right*. This means that if we have any expression like, say, `x = x + 1`, what we are doing is taking the old value of `x`, adding one to it, and storing this new result back into `x`. In short, we are "incrementing" x: increasing its value by one, no matter what `x`'s original value was.

### A few shortcuts

Needing to operate 'in place' (in other words, storing the result back inside the original variable) is quite common in programming - so common that most languages include short-hand syntax for these kind of operations. Some examples are shown below.

| Long-Hand Syntax | Short-Hand Syntax |
|------------------|-------------------|
| `x = x + 1`      | `x += 1` |
| `x = x - 5`      | `x -= 5` |
| `x = x * 2`      | `x *= 2` |
| `x = x / 10`     | `x /= 10` |
| `x = x % 10`     | `x %= 10` |
| `x = x + 1`      | `x = x++` |

---

