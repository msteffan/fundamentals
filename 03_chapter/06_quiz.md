**WDI Fundamentals Unit 3**

---

How do you create a variable called 'name' in Javascript?
- [ ] var name = "John";
- [x] touch "John";
- [ ] echo $NAME
- [ ] none of the above

> Not quite.
> In JS, variables are created by the variable name and a value, separated by an equals sign (=). Some types of variables require you to write "var" before the variable name, and some types do not.

`x = 0;x = x + 1;x = x + 2;x = x + 3;x = x + 4;x = x + 5;x = x + 6;x = x + 7;` What is the final value of x?
- [ ] 7
- [ ] 0
- [x] 28
- [ ] 23

> Let's break this down line by line.
> Line 1: x = 0
> Line 2: x = 0 + 1 = 1
> Line 3: x = 1 + 2 = 3
> Line 4: x = 3 + 3 = 6
> Line 5: x = 6 + 4 = 10
> Line 6: x = 10 + 5 = 15
> Line 7: x = 15 + 6 = 21
> Line 8: x = 21 + 7 = 28

---

`var num = 2;var num2 = 6;num2 = num * (num2 - num);console.log(num2);` What would this code print out?
- [ ] 2
- [ ] 4
- [ ] 6
- [x] 8

> Not quite.
> num * (num2 – num)  is equal to (2 * (6 – 2)) which evaluates to  8.
> So num2 = 8.

---

{% exercise %}
Create a variable x equal to the sum of a and b divided by c and finally multiplied by d. HINT: don't forget to declare the new variable "x" `var x = ( (a + b) / c ) * d;`

Add up the different names so that the fullName variable contains John's complete name.

`var fullName = firstName + " " + lastName;`

> Not quite.
> To create a string that contains John's complete name, you would need to add the firstName variable and the lastName variable, with a space in between (otherwise  you'd create JohnSmith).
{% endexercise %}

[Here are some more exercises to help you practice.](07_exercise.md)
