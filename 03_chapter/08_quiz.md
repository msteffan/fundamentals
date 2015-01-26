**WDI Fundamentals Unit 3**

---

### Test Yourself
Can you predict how the following expressions will be evaluated? Check your answers in repl.it.
* `1 || true`
* `3 || null`
* `!("")`
* `false && undefined`
* `true && !0`
* `null || 3`

One of the most common use-cases of this is when you're not sure if a variable has been assigned a value. Suppose that `x` represents some input that you've gotten from a user. If the user hasn't given any input, `x` might be `null`.

To compensate for this, we might write the expression `x = x || 10;`. If x has some 'truthy' value, the OR operator will evaluate to `x`, so it would be as if we wrote `x = x`. However, if x were `null`, the OR operator would evaluate to 10 (because `null` is 'falsey'). It's as if we've said "If x doesn't already have a value assigned, set it equal to 10". For that reason, this kind of operation is often called 'conditional assignment'.
