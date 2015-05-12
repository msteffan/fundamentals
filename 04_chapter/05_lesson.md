**WDI Fundamentals Unit 4**

---

We've covered how we can tell our programs to make decisions; now let's look at how we can tell our programs to take repeated/ongoing actions.

## The `while` Loop

To tell your program to repeat something, you use a tool called a **loop** - once your program has finished running a block of code, it 'loops' back to the beginning and starts again.

Suppose that we were to take our `if` statement from the previous lesson and loop it back on itself. Here's the flow diagram for the `if`, in case you've forgotten it.

![Flow Chart for `If` Statement](../assets/chapter4/flow_chart_if.png)
<br>

We're going to make one small (but very important) change to this - instead of advancing to the next bit of code after executing the block, we will loop back to our condition.

![Flow Chart `If` -> `While`](../assets/chapter4/flow_chart_if-to-while.png)
<br>

Now, we have a loop - so long as our condition remains true (or at least truthy), we will continue to run that block of code over and over again. This type of loop is called a `while` loop, and can be found in nearly every programming language. Here's the general rule for how a while loop is written in JavaScript.

```javascript
while (someCondition) {
  // A block of code.
}
```
As you can see, it is written in almost exactly the same way as an `if` statement.

### Test Yourself
* Consider the following code.

```javascript
var x = 10;
while (x > 5) {
  x -= 2;
}
```

How many times will this loop run? What will the final value of `x` be when it finishes?

* Here's another loop.

```javascript
var x = 10;
var y = 1;
while (x < 20) {
  y += 1;
}
```

How many times will this loop run? What happens when you try to run this code?


A while loop can run **indefinitely** as long as your condition remains true; this is usually a bad thing, so when using a while loop, it's **very important** to plan out beforehand how you will 'escape' the loop by making your condition evaluate to `false`.

Consider the following example.

```javascript
var z = 0;
var myString = '';
while (z < 5) {
  myString += 'X';
  z += 1;
}
```

Q: How many times does this loop run? What's the final value of myString?

A: Each time this loop runs, the value of `z` increases by 1; since its initial value is 0, and the condition becomes `false` the moment that z becomes 5, this means that our loop runs exactly 5 times. As a result, the string `myString` has a final value of "XXXXX" (5 Xs).

Confused? Here's the play-by-play.
* `z` is set to 0 and `myString` is set to "".
* `z` is 0, therefore <code>z < 5</code> is true so the block gets executed.
  * (in the block) "X" gets added to the end of `myString`; it is now "X"
  * (in the block) `z` is increased by 1; it is now 1. Now that the block is done, we go back to the condition.
* `z` is 1, therefore <code>z < 5</code> is true so the block gets executed.
  * (in the block) "X" gets added to the end of `myString`; it is now "XX"
  * (in the block) `z` is increased by 1; it is now 2. Now that the block is done, we go back to the condition.
* `z` is 2, therefore <code>z < 5</code> is true so the block gets executed.
  * (in the block) "X" gets added to the end of `myString`; it is now "XXX"
  * (in the block) `z` is increased by 1; it is now 3. Now that the block is done, we go back to the condition.
* `z` is 3, therefore <code>z < 5</code> is true so the block gets executed.
  * (in the block) "X" gets added to the end of `myString`; it is now "XXXX"
  * (in the block) `z` is increased by 1; it is now 4. Now that the block is done, we go back to the condition.
* `z` is 4, therefore <code>z < 5</code> is true so the block gets executed.
  * (in the block) "X" gets added to the end of `myString`; it is now "XXXXX"
  * (in the block) `z` is increased by 1; it is now 5. Now that the block is done, we go back to the condition.
* `z` is now 5, therefore <code>z < 5</code> is now **false** (since 5 is **not** less than 5) so the block does not get executed again.
* We're done!

What's most interesting about this kind of setup is that if we changed that condition from <code>z < 5</code> to <code>z < 10</code>, or <code>z < 100</code>, the loop would change to run exactly 10 or exactly 100 times, respectively. In effect, we have changed the `while` loop so that it always runs for a fixed, precisely controllable number of times - it will never get stuck in an infinite loop.

This kind of setup is so useful, and gets used so frequently, that most languages include a special kind of loop used for just this kind of behavior, called a `for` loop.

## The `for` Loop

Let's make a few modifications to our while loop from earlier.

![Flow Chart for `For` Loop](../assets/chapter4/flow_chart_while-to-for.png)

As you can see, there are a couple of key ingredients to making our `for` loop work. We need
1. an 'initialization', which sets up a starting situation (e.g. var x = 0)
2. a condition, which gets evaluated each time we're about to execute the block (e.g. x < 10)
3. a 'finalExpression', which gets evaluated immediately after the block executes *but before the condition is evaluated again* (e.g. x += 1;)

The general syntax for a `for` loop is

```javascript
for (initialization; condition; finalExpression) {
  // A block of code.
}
```

### Test Yourself

```javascript
var x = 10;
for (var i = 0; i < x; i += 1) {
  console.log('HELLO'); // This is a command to our console, telling it to display the text 'HELLO' and advance to a new line.
}
```

* How many times will 'HELLO' be printed out in the console?
* What if (all else the same) we changed the starting value of `i` to 1 instead of 0? How many times would `HELLO` get printed to the console?
* What if (all else the same) we changed the condition from <code>i < x</code> to <code>i <= x</code>?
* What if (all else the same) we changed the final condition from <code>i += 1</code> to <code>i += 2</code>?
Check your answers in repl.it.

---

Feeling good about loops? [Let's do another exercise.](07_exercise.md)
