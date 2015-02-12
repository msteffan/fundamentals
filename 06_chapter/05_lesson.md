**WDI Fundamentals Unit 6**

---

# Iterating Over Arrays

  In the past few units, we've only been able to operate on one value at a time. One of the most useful things about a collecttion (and arrays in particular) is that, if we structure our code correctly, we can actually perform the same operation on *a set of values*. This process is called **iteration** - doing something over and over and over again for every element in a set.

  There are several ways that this can be done.

  ## Iterating with Loops
  One of the most common patterns in old-school programming is using loops to iterate through an array.
  Suppose that we were given an array of starting values to work with - say, temperatures in degrees Fahrenheit - and wanted to convert them into another set of values - say temperatures in degrees Celcius - which would then be stored in a separate array.
  ```javascript
    var temps_in_f = [100, 72, 88, 15, 25, 32];
    var temps_in_c = [];
  ````
  The formula for converting between Fahrenheit and Celcius temperatures is *C = (5/9 * F)  - 32*, where F is the temperature in degrees Fahrenheit and C is the temperature in degrees Celcius. Because this is an operation that we'd like to do frequently, we might create a function for it like the one below.
  ```javascript
    function fahrToCelc(degrees) {
      return degrees* 5 / 9  - 32;
    }
  ```
  So how do we go about operating on the elements in `temps_in_f`? Well, we could just start at the beginning and work our way through, one value at a time. The first operation we'd perform is `fahrToCelc(temps_in_f[0])`

  To add this value to `temps_in_c`, we can use a built-in function that all arrays have called `push()`. Push will take whatever value is passed in as a parameter and add it as the last element of the array. For example, if we have an array called `my_array` equal to `[1,2,3]`, calling `my_array.push(4)` will change `my_array` so that it equals `[1,2,3,4]`. If `my_array` were empty, push would set that new element as its first element.
  ```javascript
    temps_in_c.push(fahrToCelc(temps_in_f[0]));
  ```
  We could then do the same thing with the next element in `temps_in_f`, listed at index 1.

---
[Test your understanding with this next quiz!](06_quiz.md)
