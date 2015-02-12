**WDI Fundamentals Unit 6**

---

# Collections - Arrays
## What is an Array?
  Arrays are one of the most basic types of collections. Essentially, an array is an ordered list of items (also known as **elements**) - one element is first, another element is second, another element is third, and so on. To select one individual element from that array, you reference its location in that order, its *index value* (or just *index*). However, there is one quirk that often throws people off about arrays: rather than starting at 1, **the first position in an array has an index of 0**.

    `my_array = ['ellen','mary','doug','pat']`
  Above is an example of an array of strings, stored in the variable `my_array`. As you can see, there are four strings contained within this array.
  The first element (index of 0) in the array is 'ellen'.
  The second element (index of 1) is 'mary'.
  The third element (index of 2) is 'doug'.
  The final element (index of 3) is 'pat'.

**NOTE** Notice how, although there are four elements in the array, the index of the last element is 3? This a result of starting our count at 0. For an array of any length, the index of the last element will be equal to that length, minus one.

  To retrieve an element from the array (say, 'pat', at index 3), simply write the following:
    `my_array[3]`
  It's almost as if we've called a function named `my_array`, passing in 3 as an input!

  Changing an element in an array is just as easy; just write an assignment operation, as if you were assigning a value to a variable.
    `my_array[3] = 'steve'`
  Just like assigning a variable, this expression will also evaluate to the value on the right.

  ### Test Yourself
  Suppose that we've defined the following array of numbers.
    `my_numbers = [4,65,0,29];`
  Assuming that each of the following expressions is evaluated in order, what will each one evaluate to?
  * `my_numbers[0]`
  * `my_numbers[1] = 10`
  * `my_numbers[2] = 5`
  * `my_numbers[1] * 2`

## Adding Complexity - Arrays of Arrays
  In addition to storing numbers, strings, or booleans as elements, arrays can go 'full-Inception' by storing *other arrays*.
    ![We need to go deeper.](http://i1.kym-cdn.com/photos/images/newsfeed/000/531/557/a88.jpg)

  Here's an example of what this can look like.
  ```javascript
  array_of_arrays = [['a','b','c'],['d','e','f'],['g','h','i']];
  ```
  You might also see it written like this - it's a bit more readable this way.
  ```javascript
    array_of_arrays = [['a','b','c'],
                       ['d','e','f'],
                       ['g','h','i']];
  ```
  Each element of `array_of_arrays` *is itself an array*. Calling `array_of_arrays[1]` will give us back the second array, `['d','e','f']`.

  Of course, what we're probably most interested in are the inner elements (strings, in this case). We could probably do the following:
  ```javascript
    var x = array_of_arrays[1]; //Evaluates to ['d','e','f']
    x[0]; //Evaluates to 'd'
  ```
  But the variable `x` there is unnecessary - it's just standing in for `['d','e','f']`. We can access that element directly from `array_of_arrays` using the following syntax.
  ```javascript
    array_of_arrays[1][0]; // Evaluates to 'd'
  ```
  If you imagine an array of arrays as a grid of values, you can think of that first index value as indicating your row and that second index value as indicating your column - essentially, a set of coordinates.

 ### Test Yourself
 Let's imagine that we're working with `array_of_arrays` from the example above. Assuming that each of the following expressions is evaluated in order, what will each one evaluate to?
 * `array_of_arrays[0][0]`
 * `array_of_arrays[1][2]`
 * `array_of_arrays[2][2] = 'z'`
 * `array_of_arrays[2][1] = array_of_arrays[1][0]`

---
[Test your knowledge of arrays in this next quiz!](03_quiz.md)
