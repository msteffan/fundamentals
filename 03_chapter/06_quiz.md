**WDI Fundamentals Unit 3**


{% exercise %}
Declare a variable called `firstName` and assign it to the value "John"
{% initial %}

{% solution %}
var name = 'John';
{% validation %}
assert(firstName == 'John');
{% context %}
var firstName;
{% endexercise %}

{% exercise %}
<pre><code>
x = 0;
x = x + 2;
x = x + 7;
</code></pre>
What is the final value of x?
{% initial %}
x =
{% solution %}
var x = 9;
{% validation %}
assert(x == answer);
{% context %}
var x, answer = 9;
{% endexercise %}

{% exercise %}
<pre><code>
var num = 2;
var num2 = 6;
num2 = num * (num2 - num);
</code></pre>
What is the final value of num2?
{% initial %}
num2 =
{% solution %}
var num2 = 8;
{% validation %}
assert(num2 == answer);
{% context %}
var num2;
var answer = 8;
{% endexercise %}

{% exercise %}
Create a variable x equal to the sum of a and b divided by c and finally
multiplied by d. HINT: don't forget to declare the new variable "x"
{% initial %}

{% validation %}
assert(x == 4);
{% solution %}
var x = ((a + b) / c) * d;
{% context %}
var a = 1;
var b = 2;
var c = 3;
var d = 4;
{% endexercise %}

{% exercise %}
Given two variables `firstName` and `lastName` assign them to a new variable
`fullName` and include a space between them.
{% initial %}
{% solution %}
var fullName = firstName + ' ' + lastName;
{% validation %}
assert(fullName == 'Dwayne Sturgeon');
{% context %}
var fullName;
var firstName = 'Dwayne';
var lastName = 'Sturgeon';
{% endexercise %}

[Here are some more exercises to help you practice.](07_exercise.md)
