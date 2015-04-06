 **WDI Fundamentals Unit 5**

---

You can use a function in any place where you would use a ________.

- [ ] argument
- [x] variable
- [ ] prompt
- [ ] parameter

> Not quite.
> Just like JavaScript Variables, Functions must be declared and can be used in
> expressions.

What does the following code print to the console?
```function square(x) { return (x * x ) }
function cube(x) {
  return (x * square(x));
}
console.log(cube(2));```

- [ ] 2
- [ ] 6
- [x] 8
- [ ] 16

> Not quite.
> The `square` function is called within the `cube` function, so the code would
> evaluate to `2 * 2 * 2` which evaluates to `8`.

What would this code evaluate to?
```function totalUp(a, b, c) {
  var tot = a + b + c;
  if (tot > 0 ) {
    return tot;
  }
}
totalUp(2, 4, 6, 8);```

- [x] 12
- [ ] 20
- [ ] 10
- [ ] 18

> Not quite.
> The correct answer was 12.
>
> The `totalUp` function takes three arguments, but was supplied with 4 arguments
> when it was invoked. When functions are called with extra arguments, JavaScript
> simply ignores the extra arguments.

BONUS: How might you write a function that gives us the biggest value from a
set of four numbers?

- [x] bonus

> There are many ways to solve this problem.
> Below is just one way to write this function in JavaScript:
> ```
> getLargest(a, b, c, d) {
>   if (a > b && a > c && a > d) {
>     return a;
>   } else if (b > a && b > c && b > d) {
>     return b;
>   } else if (c > a && c > b && c > d) {
>     return c;
>   } else {
>     return d;
>   }
> }
> ```

---


Nice job! [Here's an exercise that should help you practice writing functions.](07_exercise.md)
