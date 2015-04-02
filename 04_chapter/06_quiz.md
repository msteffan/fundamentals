**WDI Fundamentals Unit 4**

---

What statement can you use to completely exit a loop and continue on through your code?*
Acontinue  Bexit  Cbreak Dend

Not quite.
A break statement will end any loop.

The second expression in a for loop usually:*
Asets the final expression Binitializes a counter Cis a condition that determines whether whether to execute the code block Dnone of the above

Not quite.
The general syntax for a 'for loop' is:
   for (initialization; condition; final expression) {
   // A block of code.
   }

That second condition gets evaluated each time we're about to execute the block.

Given this while loop:

```
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

What is the first line that this loop would produce?*
Hint: If you ran this code in the console, the first line in the result would be...

How many lines would be produced by the loop?*
HINT: How many times would the console run through the loop before finishing?
A0  B1  C2  D3  E4  F5

What is the last line that this code would produce?*
Hint: If you ran this code in the console, the last line that would appear is...

Not quite.
The last line that would appear would be "Exiting the loop!":

```
Entering the loop
2
3
4
5
Exiting the loop
```

---


Feeling good about loops? [Let's do another exercise.](07_exercise.md)
