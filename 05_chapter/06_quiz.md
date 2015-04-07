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

---

Read the following code and then answer the questions below.

```js
function square(x) { return (x * x ) }
function cube(x) {
  return (x * square(x));
}
console.log(cube(2));
```

---
What does the above code print to the console?

- [ ] 2
- [ ] 6
- [x] 8
- [ ] 16

> Not quite.
> The `square` function is called within the `cube` function, so the code would
> evaluate to `2 * 2 * 2` which evaluates to `8`.

---

Read the following code and then answer the questions below.

```js
function totalUp(a, b, c) {
  var tot = a + b + c;
  if (tot > 0 ) {
    return tot;
  }
}
totalUp(2, 4, 6, 8);
```
---

What would the above code evaluate to?

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

---

{% exercise %}
How might you write a function called `maxNumber`
that gives us the biggest value from a
set of four numbers?
{% initial %}
function maxNumber(a, b, c, d) {
  // Your code
}
{% solution %}
// One solution
function maxNumber(a, b, c, d) {
  if (a > b && a > c && a > d) {
    return a;
  } else if (b > a && b > c && b > d) {
    return b;
  } else if (c > a && c > b && c > d) {
    return c;
  } else {
    return d;
  }
}
{% validation %}
assert(maxNumber(4, 5, 6, 7) == findMax(4, 5, 6, 7));
{% context %}
var maxNumber;
function findMax(args) {
  if ( !Array.isArray(args) ) {
    args = Array.prototype.slice.call(arguments);
  }
  var max = null;
  for (var i = 0, len = args.length; i < len; i++) {
    if ( args[i] >= max ) {
      max = args[i]
    }
  }
  return max;
}
{% endexercise %}

---


Nice job! [Here's an exercise that should help you practice writing functions.](07_exercise.md)
