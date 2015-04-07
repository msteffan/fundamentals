**WDI Fundamentals Unit 4**

---

What statement can you use to completely exit a loop and continue on through
your code?
- [ ] continue
- [ ] exit
- [x] break
- [ ] end

> Not quite.
> A break statement will end any loop.

The second expression in a for loop usually:
- [ ] sets the final expression
- [ ] initializes a counter
- [x] is a condition that determines whether whether to execute the code block
- [ ] none of the above

> Not quite.
> The general syntax for a 'for loop' is:
> ```
> for (initialization; condition; finalExpression) {
>   // A block of code.
> }
> ```
> That second condition gets evaluated each time we're about to execute the block.

---

Read the following code and then answer the questions below.

```js
var x = 1;
console.log('Entering the loop');
while (x < 20) {
  if (x == 5) {
    break;
  }
  x = x + 1;
  console.log('Exiting the loop');
}
```

---

What is the first line that the above loop would produce?<br><small>Hint: If you ran this code in the console, the first line in the result would be...</small>

- [x] Entering the loop
- [ ] 5
- [ ] Exiting the loop

> Not quite.
>
> The first thing printed to the console would be 'Entering the loop'

How many lines would be produced by the loop?<br><small>HINT: How many times would the console run through the loop before finishing?</small>
- [ ] 0
- [ ] 1
- [ ] 2
- [ ] 3
- [x] 4
- [ ] 5

> Not quite.
> The while loop would run 4 times, producing the numbers:
> ```
> Entering the loop
> 2
> 3
> 4
> 5
> ```

What is the last line that this code would produce?<br><small>Hint: If you ran this code in the console, the last line that would appear is...</small>

- [ ] Entering the loop
- [x] Exiting the loop
- [ ] 5

> Not quite.
> The last line that would appear would be "Exiting the loop!":
> ```
> Entering the loop
> 2
> 3
> 4
> 5
> Exiting the loop
> ```

---


Feeling good about loops? [Let's do another exercise.](07_exercise.md)
