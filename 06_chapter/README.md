**WDI Fundamentals Unit 6**

---

#####By the end of this Unit, you'll be able to:
* Create collections (arrays and associative arrays) and retrieve values from them
* Operate on all the elements within a collection using loops and iterators
* Explain how arrays and associative arrays differ

---

Congratulations, you've almost made it to the end of WDI Fundamentals!

In Unit 5, you learned to create your own functions that could generate specific behaviors. If you wanted to get the average of three variables, `x`, `y`, and `z`, you could write the following:

```javascript
  function avgOfThree(x,y,z) {
    return (x + y + z)/3;
  }
```

However, this is a *very* specific use case. What if you wanted to be able to find the average of ten numbers? Try to modify [the code in repl.it](http://repl.it/bJM) like so:
```javascript
  function avgOfTen(a,b,c,d,e,f,g,h,i,j) {
    return (a + b + c + d + e + f + g + h + i + j)/10;
  }
```
Ok, now try writing `function avgOfOneHundred()`.

Or don't. It would be exhausting to write a hundred different identical variations of this function. The more variables we want to keep track of, the more code we have to write – the length of our code is growing even though our program is not growing in complexity.

To keep our code DRY (as we learned in the [last Unit](../05_chapter/05_lesson.md)), we should hand our function a *set* of values (of any size) and tell it to work with that.

We can do this using a type of data called a **collection**.

Collections, as the name implies, are groups of (generally, similar) values.

Here are some examples of real world collections:
- a list of groceries to buy
- a stack of books to read
- a queue of people waiting to get into a movie

In this unit, we will see how all of these things (and more) can be turned into collections – both ordered collections and unordered collections – and why this is a really important tool to add to your belt.


[Let's get started.](02_lesson.md)
