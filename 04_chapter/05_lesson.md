**WDI Fundamentals Unit 4 - Flow Control**

---

## Loops

When you're dealing with arrays, sometimes you need to perform the same action for all the items in an array, that's why we use loops. Loops are sets of instructions used to repeat the action (a block of code) until a condition break the execution of the loop.

JavaScript supports two loop statements: `for` and `while`. The For statements are best used when you want to perform a loop a specific number of times.

The While statements are best used to perform a loop an undetermined number of times.


In addition, you can use the `break` and `continue` statements within loop statements.


#### For Loop

The "for" loop is a JavaScript "method" that allows a certain action (ie: block of code) to be performed continuously in a variably controlled fashion. It is very similar to a "while" loop in which lines of JavaScript codes can be grouped together and repeated until a certain condition.

Pseudo Code
```
for ([var i = startValue];[i < endValue]; [i+=stepValue]) {
    // Your code here
}
```

Javascript:

```
var i;
for (i = 0; i <= 10; i++) {
    console.log(i); // Prints the numbers from 0 to 10
}
```

In the code above, the code between the `{}` will be executed 11 times, because end value (`i <= 10`) has to be less or equal than 10, which means the execution of the loop will start with a value 0, then it will be incremented to 1,2,3,4,5,6,7,8,9 and 10, then the condition to loop will be false.



#### While Loops

You use while loops, if you don't know how often you'll loop.

Pseudo-code

```
while (condition) {
  // Your code here
}
```

A while loop is similar to an if statement, except that the code will be executed until the condition evaluates to a falsy value.

When a while loop begins, the JavaScript interpreter checks if the condition statement is true. If it is, the code between the curly braces is executed. At the end of the code block (ending by `}`) , the while loop loops back to the condition statement and begins again.

If the condition statement is always True, then you will never exit the while loop, so be very careful when using while loops!

```
var x = 0;
while (x < 5) {
  console.log(x);
  x++;
}
```
In the situation above, the code between the curly braces will be executed 5 times, and the value of the variable `x` will be 0,1,2,3,4 then the condition between parenthesis will be false.

```
var x = 10;
while (x <= 5) {
    console.log(x);
    x++;
}
```
In this example, the code will never be executed, x will never be less or equal than 5, the condition will always be false.

```
var x = 0;
while (x <= 5) {
  console.log(x);
}
```
Last example, this code will be infinitely executed, because the condition will always be true, and we don't change the value of x in the code between curly braces.
