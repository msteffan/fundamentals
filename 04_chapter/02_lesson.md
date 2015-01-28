**WDI Fundamentals Unit 4 - Flow Control**

---

##Conditionals


When you write code , you want to execute code based on conditions. A condition, most of the time is wether a comparison will be true or false (ie. `4 > 5` will be false, because the number 4 is not superior to the number 5). Based on this kind of conditions, we are going to execute some code if the condition is true, or some other code if the condition is false.

Javascript supports differents types of conditions :
* `if`
* `if else`
* `if else if`
* `switch`


#### If ... Else Statement

The `if` Statement is a way to make decisions based on the truthiness or falsiness of a statement. An `if` statement can optionally be followed by an `else` clause that will be executed if the condition in the `if` is false. The syntax for the if statement looks as follows:

Pseudo-Code :
```
if (condition) {
   statements_1
}
```

Javascript :
```
a = 2;
b = 2;

if (a + b == 5) {
   alert("a + b is equal to five");
}
```

In this situation, the code between the curly braces (`{}`), will not be executed, because the code in the `condition` will always return false, 2 plus 2 is not equal to 5.

We can add an else statement to this `if` :

Pseudo-Code :
```
if (condition) {
  statements_1
} else {
  statements_2
}
```

Javascript :
```
a = 2;
b = 2;
if (a + b == 5) {
  alert("a + b is equal to five");
}else{
  alert("Wrong Operation ! a + b is NOT equal to five");
}
```

Because the code in the `condition` will return false, javascript will then execute the code for the else condition.


#### If ... Else ... if Statement

You may also compound the statements using `else if` to have multiple conditions in sequence. You should use this conditions if you want to select one of many sets of lines to execute.

Pseudo-Code :
```
if (condition) {
  statements_1
} else if (condition_2) {
  statements_2
}
```

Javascript :
```

a = 2;
b = 4;

if (a + b == 5) {
  alert("a + b is equal to five");
}else if (a + b == 6){
  alert("a + b is equal to six");
} else {
  alert("a + b is equal to something different than 5 or 6");
}
```

#### Switch Statement

As we've seen before, we can choose which condition will be executed using `if...else...if`, but if we have a lot of conditions, the code become a bit repetitive and hard to read, for example :

```
// day of the week in a number, sunday is 0, saturday is 6
dayNumber = 1
if(dayNumber == 0){
  day = "Sunday";
} else if(dayNumber == 1){
  day = "Monday";
} else if(dayNumber == 2){
  day = "Tuesday";
} else if(dayNumber == 3){
  day = "Wednesday";
} else if(dayNumber == 4){
  day = "Thursday";
} else if(dayNumber == 5){
  day = "Friday";
} else if(dayNumber == 6){
  day = "Saturday";
} else {
  day = null;
  alert("wrong value for day");
}

```

The code above does what we expect, which means after this conditionnal statement is executed, the value of the variable day will be either the corresponding string for a given number between 0 and 6 (so 7 possible values) or null if the number is un-recognized.

But this code is not easy to read, and a lot of code is repeated (`} else if(dayNumber == X){` is repeated 7 times), for example , if the name of the variable `dayNumber` changes, we will need to update it 8 times in the code, this is not really efficient. For this purpose, when you need to handle a lot (more than 3) cases, you should use a `switch` statement:

```
dayNumber = 1

switch (dayNumber) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
    break;
  default:
    day = null;
  alert("wrong value for day");
}
```

This looks better, no ? The code above is doing exactly the same than the version with `if..else..if` but in a much shorter and readable version.

Javascript will evaluate the value of the variable `dayNumber` and execute the code between the corresponding `case` and `break`.

If there is no `break` at the end of a `case`, then javascript will execute the following cases even if the value of the next `case` is not the same than the variable value.

If there is no `case` corresponding to the value of the variable, then the code after `default` will be executed, `default` doesn't include a `break` because it's the last one in the `switch` statement.
