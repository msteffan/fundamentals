**WDI Fundamentals Unit 6**

---

# Iterating Over Arrays

  In the past few units, we've only been able to operate on one value at a time. One of the most useful things about a collecttion (and arrays in particular) is that, if we structure our code correctly, we can actually perform the same operation on *a set of values*. This process is called **iteration** - doing something over and over and over again for every element in a set.

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
  So how do we go about operating on the elements in `temps_in_f`? Well, we could just start at the beginning and work our way through, one value at a time.
  ```javascript
    temps_in_c.push(fahrToCelc(temps_in_f[0]));
  ```
  Then, we could run an almost identical command to operate on every subsequent element in `temps_in_f`.
  ```javascript
    temps_in_c.push(fahrToCelc(temps_in_f[1]));
    temps_in_c.push(fahrToCelc(temps_in_f[2]));
    temps_in_c.push(fahrToCelc(temps_in_f[3]));
    temps_in_c.push(fahrToCelc(temps_in_f[4]));
    temps_in_c.push(fahrToCelc(temps_in_f[5]));
  ```
  However, this code is extremely repetitious, and it also forces us to hard-code exactly how many times we want the operation to be performed. It'd be better if there were a way to run this code exactly as many times as there are elements in the first array. Fortunately, there is a tool perfectly suited for this task - our old friend the `for` loop.
  ```javascript
    for (var i = 0; i < temps_in_f.length; i += 1) {
      temps_in_c.push(fahrToCelc(temps_in_f[i]));
    }
  ```
  By starting our count at zero, stopping before `i` reaches the length of the array, and increasing `i` by one every time, we can hit every element in our array in ascending order and perform the same operation on each one sequentially.

  However, we could just as easily have gone in the opposite direction - starting at the last element, and ending with the first - simply by specifying different settings for the `for` loop:
  ```javascript
    for (var i = (temps_in_f.length - 1); i >= 0; i -= 1) {
      temps_in_c.push(fahrToCelc(temps_in_f[i]));
    }
  ```

  We could even operate only on every third element, like so:
  ```javascript
    for (var i = 2; i < temps_in_f.length; i += 3) {
      temps_in_c.push(fahrToCelc(temps_in_f[i]));
    }
  ```

  Despite being one of the most basic ways to iterate through an array, in JavaScript (and many other languages) this is also one of the most versatile ones!

  ### Test Yourself
  Create a new repl.it session with the following JavaScript code:
  ```javascript
    var old_array = [12,45,6,23,19,20,20,15,30,42];
  ```
  How could you use iteration to generate a new array called `new_array` from `old_array`, so that...
  * Each value in `new_array` is the value of its corresponding element in `old_array`, plus 5?
  * Each value in `new_array` is the square of the value of its corresponding element in `old_array`?
  * Every **odd-indexed** value in `new_array` is *double* its corresponding elemnt in `old_array`, while every **even-indexed** value is unchanged?
  * `new_array` is the exact mirror image of `old_array`?

  These ones are a bit tricky, so don't get discouraged if the answers don't come immediately; just keep experimenting with your code until it works!


---
Feeling confident? [Test your understanding with this next quiz.](06_quiz.md)
