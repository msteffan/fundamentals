**WDI Fundamentals Unit 6**

---

#####By the end of this Unit, you'll be able to:
* Create collections (arrays and associative arrays) and retrieve values from them.
* Operate on all the elements within a collection using loops and iterators.
* Explain how arrays and associative arrays differ.

---

Congratulations, you've almost made it to the end of 'Fundamentals'!

In Unit 5, you learned to create your own functions that could generate specific behaviors. If you wanted to get the average of three variables, `x`, `y`, and `z`, you could write the following:
```javascript
  function avgOfThree(x,y,z) {
    return (x + y + z)/3;
  }
```
However, this is a *very* specific use case. What if you wanted to be able to average five numbers? Ten? A hundred? It clearly doesn't make sense to write a hundred different almost-identical variations of this same function. It'd be much more straightforward if we could simply hand our function a *set* of values (of any size) and tell it to work with that. Fortunately, we *can* do this, using a type of data called a **collection**.

Collections, as the name implies, are groups of (generally, similar) values. Things like this are commonplace in the real world:
a list of groceries to buy; a stack of books to read; a queue of people waiting to get into a movie. In this unit, we will see how all of these things (and more) can be easily modeled in a program using a collection. And at the end of the unit, we'll segue into the how you can use collections to define totally custom kinds of data.

[Let's get started.](02_lesson.md)
