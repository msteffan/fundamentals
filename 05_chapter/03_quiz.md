 **WDI Fundamentals Unit 5**

---
What value will be returned from the function below when x is equal to 25?
```function myFunction(x) {
  if (x > 30) {
    return x - 30;
  } else if (x < 10) {
    return x;
  }
}```

- [ ] 25
- [x] 24
- [ ] 9
- [ ] 10

> Not quite.
> If x is equal to 25, then the function would execute the final return
> statement, x – 1.  And since x equals 25, that statement would evaluate to 24.

What value will be returned from the function below when x is equal to 10?
```function myFunction(x) {
  if (x > 30) {
    return x - 30;
  } else if (x < 10) {
    return x;
  }
}```

- [ ] 25
- [ ] 24
- [x] 9
- [ ] 10

> Not quite.
> If x is equal to 10, then the function would execute the final return
> statement, x – 1.  Which, if x equals 10, evaluates to 9.

How would we call this function, either in our program or the console, passing
5 as an argument?

- [ ] var myFunction() = 5;
- [ ] myFunction(5);
- [ ] myFunction(x) { return 5; }
- [ ] myFunction[5];

> Not quite.
> Javascript functions are executed or "called" by appending () to the function
> name. To call this function with 5 as an argument, we would write:
> `myFunction(5)`

This function compares two numbers, x and y.
How would we call this function to compare 10 and 20?
```function anotherFunction(x, y) {
  return (x < y ) ? x : y;
}```

- [ ] anotherFunction(x, y)
- [x] anotherFunction(10, 20)
- [ ] anotherFunction[10, 20]
- [ ] anotherFunction[x, y]

> Not quite.
>
> To invoke the funciton you pass 10 and 20 as arguemnts.
> `anotherFunction(10, 20)`

What would we expect to get back if, from the last question, we compared 10 and 20?

- [ ] true
- [ ] false
- [x] 10
- [ ] 20

> Not quite.
> If x is 10 and y is 20, then the conditional statement would evaluate to true,
> and the ternary operator would return the 'truthy' value x which evaluates to 10.

---


[Let's practice functions a bit more with some exercises.](/04_exercise.md)
