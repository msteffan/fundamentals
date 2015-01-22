**WDI Fundamentals Unit 4**
---

##Conditionnals and loops 


### Conditionnals

When you write code , you want to execute code based on conditions. A condition, most of the time is wether a comparison will be true or false (ie. `4 > 5` will be false, because the number 4 is not superior to the number 5). Based on this kind of conditions, we are going to execute some code if the condition is true, or some other code if the condition is false.

Javascript supports differents types of conditions :
* `if`
* `if else`
* `if else if`
* `switch`

#### Truthy / Falsy values

Developers often talk about "truthy" or "falsy" values. Conditionnal Statements are based on the "Truthiness" of "Falsiness" of a value. This doesn't mean that the value has to be explicitely true or false, this means that the "coerced" value (the value converted to a boolean) will be true or false. For example, the integer `0` converted to a boolean will be false, but the string `"0"` converted to a boolean will be true. Conditions can be made with lots of differents cases, for example, you might have a script that checks if a Boolean value is true or false, if variable contains number or string value, if an object is empty or populated, or even check type and version of the visitors browser.

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