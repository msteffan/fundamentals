**WDI Fundamentals Unit 6**

---

In JavaScript, how would we access the second element in the array called "myArray"?

- [ ] myArray[2]
- [ ] myArray(2)
- [x] myArray[1]
- [ ] myArray(1)

> Not quite.
> To access the second element in an array, you would need to use the command:
> myArray[1]
> Remember that the first element in an array has an index of 0.

After the following code has executed, what does the fruits array contain?
```var fruits = ['apple', 'orange', 'banana'];
fruits.pop();
fruits.push('grape');
fruits.push('banana');```

- [ ] ['apple', 'orange', 'banana']
- [ ] ['orange', 'banana', 'grape', 'banana']
- [x] ['apple', 'orange', 'grape', 'banana']
- [ ] ['banana', 'grape', 'apple', 'orange']

> Not quite.
> This code would remove "banana", add "grape" and then add "banana" back to the last position of the array.

What would 'ages[2];' evaluate to? ```var ages = [26, 28, 30, 28, 17];```
- [ ] 26
- [ ] 28
- [x] 30
- [ ] 17

> Not quite.
> ages[2] would return the element "30".

What would 'ages.indexOf(28);' evaluate to?
- [ ] 0
- [x] 1
- [ ] 2
- [ ] 3
- [ ] 4
- [ ] 5

> Not quite.
> .indexOf() returns the first – least – index of an element within the array
> equal to the specified value, or -1 if none is found.  So .indexOf(28) would
> evaluate to 1.

---
[Let's get some practice with creating and editing arrays.](04_exercise.md)
