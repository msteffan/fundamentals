**WDI Fundamentals Unit 4**

Read the following code and then answer the questions below.

```js
var age = 32;
if (age < 21) {
    console.log('Come back when you are older!');
} else if (age < 50) {
    console.log('Thank you. Come on in.')
} else {
    console.log('No need to card you, right this way!');
}
```

---
What will console.log print out if `age` is 32?

- [ ] Come back when you are older!
- [x] Thank you. Come on in.
- [ ] No need to card you, right this way!

> Not quite.
> If age equals 32, then age is greater than 21 and less than 50, yielding the message, "Thank you. Come on in!"

---

Read the following code and then answer the questions below.

```js
var isHungry = false;
var hasFoodInFridge = true;
if ( /* Your Expression */) {
    console.log('I need to buy food now!');
}
```
---

Let's assume that you need to buy food if <br>a) you're hungry AND <br>b) there is no food in the fridge.
Which of the conditions below should you use in the if statement
(replacing `"/ * Your Expression */"`) to print the message 'I need to buy food now!'?
- [ ] `isHungry && !hasFoodInFridge`
- [x] `!isHungry && hasFoodInFridge`
- [ ] `isHungry || !hasFoodInFridge`
- [ ] `isHungry && hasFoodInFridge`

> Not quite.
> In order for the condition to evaluate to truthy, it would need to be written so that both are true. "!isHungry || hasFoodInFridge"

---

Read the following code and then answer the questions below.

```js
var flower = prompt('What type of flower do you like?');
switch (flower) {
    case 'rose':
        console.log(flower + ' costs $2.50');
        break;
    case 'daisy':
        console.log(flower + ' costs $1.25');
        break;
    case 'orchid':
        console.log(flower + ' costs $1.50');
        break;
    default:
        console.log('There is no such flower in our shop');
        break;
}
```

---

What would the above code print out if the user's input was "orchid"?

- [ ] flower costs $1.50
- [ ] flower costs $2.50
- [ ] orchid costs $2.50
- [x] orchid costs $1.50

> Not quite.
> The switch statement would execute the first case that matches the 'flower' variable. We know the user inputted "orchid", so var flower = "orchid".
> The code that would be executed for the matching "orchid" case is "`flower` + " costs $1.50", which evaluates to "orchid costs $1.50".

What would the above code print out if the user's input was "tulip"?
- [ ] flower costs $2.50
- [ ] tulip costs $2.50
- [ ] tulip costs $1.25
- [x] There is no such flower in our shop

> Not quite.
> The user's input "tulip" does not match any of the cases in this code – so the switch statement would evaluate the default case, printing "There is no such flower in our shop".

---

Think you've got it? [Let's do an exercise to cement what we've learned.](04_exercise.md)
