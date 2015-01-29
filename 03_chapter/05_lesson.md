**WDI Fundamentals Unit 3**

---
# Expressions with Variables

One major calculator function that we haven't mentioned so far is `memory` - many calculators have buttons that can be used to store the results of calculations in memory for later use. JavaScript's answer to this is **variables**.

Suppose that we wanted to save the result of our expression, `(99*746)-(837*23)`, and then multiply the whole thing by two later. We could store that result in a variable `x` using `=` (the 'assignment' operator) as follows:

`x = (99*746)-(837*23);`

When we want to then use this result, we simply subsitute `x` for wherever our original expression might have gone; for instance, we could write `x * 2;`, and this expression would evaluate to double whatever value was stored in `x`.

To figure out how to evaluate an expression containing variables, we simply draw a tree, as before - the only difference is that `x` (or whatever other variable we might be using) evaluates to whatever value it's storing at the time.

#### Test Yourself
Assume that `x` is equal to 10. What values do the following expressions evaluate to? Check your answers in repl.it.
* `x + 20`
* `x * x`
* `3 * (x * x) - 2 * x + 5`

> In JavaScript, a variable can be defined in one of two ways:
>  `var x = 10;`
>  `x = 10;`
> For now, just recognize that either of these will allow a variable to be created. However, the implications of using one vs the other are actually quite significant, and will be covered later on in this assignment (when we get to the topic of **scope**).

We can redefine our variable `x` as many times as we want. However, ***only the most recent value of `x` is retained*** - once `x` gets redefined, its original value is lost forever.

Suppose we ran the following lines of code in order, one by one.
```javascript
  x = 10;
  x = 1;
  x = 5;
  x = 15;
  2 * x;
```
What does that last expression evaluate to? Or, put differently, what is the most recent value of x (as of that line) multiplied by 2? If you guessed 30, then you're correct!

> *Incidentally, in addition to allowing us to assign values to variables, `=` is also an operator, and it outputs a value after it's finished its 'assignment' work. In particular, the `=` operator evaluates to whatever the expression to the right of the `=` evaluates to. In other words, the expression `x = 2` evaluates to `2`. And since these operations can be inputs to other operations, you may sometimes see expressions like*

>  `(x = 2) * 5`

> *`x = 2` will first set `x` to 2, and then evaluate to 2; this result then gets multiplied by 5, causing the whole expression to evaluate to 10.*

Sometimes, we find variables on both sides of the `=`. Suppose we have two variables, `x` and `y`, as in the example below.

```javascript
  x = 5;
  var y = 10;
  x = y + 10;
```

What happens in that third line? For starters, everything to the right of the `=` must be evaluated before any kind of assignment can happen. `y + 10` evaluates to 20, so what we're left with is the expression `x = 20`. This assigns the value 20 to `x`, and the entire expression evaluates to 20.

Let's look at one more example using the same two variables, `x` and `y`.
```javascript
  x = 1;
  y = 10;
  x = y * 2;
  y = x + 1;
  x = y + 1;
  y = 2 * x;
```
Feeling dizzy? Don't worry, we'll step through this one together.

  __Line 1__: We assign `x` the value 1.

  __Line 2__: We then assign `y` the value 10.

  __Line 3__: As of this point in the code, `y`'s value is 10, so we now redefine `x` and assign it the value 20.

  __Line 4__: `x`'s current value is 20, so `y` gets assigned a new value of 21.

  __Line 5__: `y` was just changed to 21, so `x` becomes 22.

  __Line 6__: `x` is now 22, so `y` becomes `2 * 22`, or 44.

One important thing to mention here is that **at no point is any lasting relationship established between x and y** (unlike how equations work in math). We are simply evaluating the expression on the right and assigning the result to the variable on the left.

### Test Yourself
Give these a try - see if you can predict the final values of `x`, `y`, and `z`. Check your answers in repl.it by copying the entire hunk of code into the editor window, running it, and then checking `x`,`y`, and `z` in the terminal.

#1
```javascript
  x = 1;
  y = 2;
  z = 3;
  x = y;
  y = z;
  z = x;
```
#2
```javascript
  x = 1;
  y = 0;
  z = -1;
  x = y + z;
  y = z * x;
  z = x - y;
  x = y * y;
  y = z * z;
  z = z - 1;
```

Whoa! That last one's pretty weird - how can z be on both sides of the `=`? What do you think happens there?

The key is remembering how the `=` operator works - before it assigns anything to the variable on the left, *it first evaluates the expression on the right*. This means that if we have any expression like, say, `x = x + 1`, what we are doing is taking the old value of `x`, adding one to it, and storing this new result back into `x`. In short, we are 'incrementing' x : increasing its value by one, no matter what `x`'s original value was.

> *Needing to operate 'in place' (in other words, storing the result back inside the original variable) is quite common in programming - so common that most languages include short-hand syntax for these kind of operations. Some examples are shown below*
>
> | Long-Hand Syntax | Short-Hand Syntax |
> |------------------|-------------------|
> | `x = x + 1` | `x += 1` |
> | `x = x - 5` | `x -= 5` |
> | `x = x * 2` | `x *= 2` |
> | `x = x / 10` | `x /= 10` |
> | `x = x % 10` | `x %= 10` |
>
> *Although JavaScript does *not* offer them, some languages (Ruby, for instance) allow you to even do this with logical operators, like OR (`||`) and AND (`&&`)!*
>
> | Long-Form syntax | Short-Hand Syntax |
> |------------------|-------------------|
> | `x = x && true` | `x &&= true` |
> | `x = x `&#124;&#124;` false` | `x `&#124;&#124;`= false` |

---
Ready for another quiz? [Here we go!](06_quiz.md)


