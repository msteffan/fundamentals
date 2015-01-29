**WDI Fundamentals Unit 3**

---

# Expression Oddballs

At this point, we've covered most of what you should know about expressions. However, there are a few quirks and exceptions that we've (until now) glossed over. Let's take a closer look at some of them.

## Undefined and Null
What happens if we try to evaluate a variable that we haven't created or assigned value to? The answer is that JavaScript will usually let us do this, but it will evaluate that variable to one of the following special values to indicate that something's gone wrong.
* **`undefined`** : When you trying to evaluate a variable that doesn't exist in your program, and JavaScript has no idea what you're referring to.
* **`null`** : When the variable that you're referencing exists, but doesn't have any value assigned to it.

## 'falsey' / 'truthy'
We've seen in the first few lessons that some operators can behave differently depending on the kind of values that they are operating on. For example, in the expression `1 + 2 + 3 + 4`, the `+` operator is performing addition; however, in the expression `"Happy birthday, " + "Tom"`, the `+` operator is working with strings, so it performs a concatentation instead.

Another example of this is the logical operators NOT(`!`), OR (`||`), and AND (`&&`); although they're primarily used with boolean values, they can also accept inputs that are strings, numbers... pretty much anything. When this happens, the logical operators categorize their inputs as being either 'falsey' and 'truthy', and (at least in JavaScript) follow the following rules to determine how to behave.
* NOT : If the input is 'truthy', give back `false`; if the input is 'falsey', give back `true`.
* OR : Give back the first 'truthy' value; if both values are 'falsey', give back the last 'falsey' value.
* AND : Give back the first 'falsey' value; if both values are 'truthy', give back the last 'truthy' value.

Here's a table to show you which kinds of values are which in JavaScript.

| 'Falsey' |  'Truthy' |
|----------|-----------|
| `false` | `true` |
| 0 | All numbers except 0, including 'Infinity' (what you get after dividing by 0) |
| Empty strings ("") | All non-empty strings |
| Undefined, Null, and NaN ('Not A Number', a special type of numeric value) | Pretty much everything else |

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

---
Ready for another [quiz](09_quiz.md)
