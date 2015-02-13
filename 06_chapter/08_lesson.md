**WDI Fundamentals Unit 6**

---

# Associative Arrays

## Organizational Systems for Arrays

So far, all of the arrays that we've seen so far have stored and managed their elements by their indices. This is a very convenient way of managing things, but it also has some disadvantages. Consider the following example.

Say we have a line of people waiting for the bus (or the latest iPhone, if you prefer.). We'll model these people using the array below.

  `['Rachel','Monica','Phoebe','Joey','Chandler','Ross']`

We can refer to each person by their position in line: Rachel is first (index: 0), followed by Monica (index: 1), Phoebe (index:2), and so on. Great! This is an easy way to keep track of who is where.

But suppose that Monica decides she's waited long enough for an iPhone, and decides to leave the line and get an Android phone instead. What happens when Monica leaves?

  `['Rachel','Phoebe','Joey','Chandler','Ross']`

Well, Rachel stays in the same place. But suddenly, Phoebe isn't at index 2 - she's now at index *1*, while *Joey* is now the one at index 2! In fact, every person after Monica ends up taking one big step forward in line, throwing all of our references into, as it were, 'disarray'.

This system does a good job of keeping track of everyone's order, but its biggest drawback is that our method of referencing any element is tied to its position *rather than the element itself*. Fortunately, there are other ways of keeping track of things - for example, labelling them.

Let's imagine that every person in this totally hypothetical office has a 'lunch' that they keep in the fridge.

|  label  |  value  |
|:-------:|:-------:|
 `'Matt'` | `'tuna sandwich'`
`'Floyd'` | `'salad'`
 `'Shannon'` | `'soup'`
 `'Josh'` | `'pasta'`

If Floyd eats his lunch, does it affect anyone else's food? Nope! The *association* between each label (read: reference) and the food (read: value) it refers to is preserved.

|  label  |  value  |
|:-------:|:-------:|
 `'Matt'` | `'tuna sandwich'`
`'Floyd'` | `null`
`'Shannon'` | `'soup'`
 `'Josh'` | `'pasta'`

This is the basic principle underlying an **associative array** (also known in some languages as *hash*). An associative array associates each value with a reference called a **key**. This system also has some drawbacks. For instance, because each key/value pair is independent of any of the others, the array doesn't keep a consistent 'order' to its elements; an associative is not the right tool for keeping track of soemthign like that. But there are definitely use cases where an associative array is an extremely valuable tool.

## Associative Arrays in JavaScript

Much like a normal array is written using square braces (`[...]`), an associative array is written using curly braces (`{...}`). Key-value pairs are separated by commas, just like individual values are in a normal array; within each of these pairs, keys are separated from their values by colons (`:`).

Here's what the 'lunches' table above might look like as an associative array.
```javascript
  var lunches = { 'Josh' : 'pasta',
                  'Floyd' : 'salad',
                  'Matt' : 'tuna sandwich',
                  'Shannon' : 'soup' };
```

Elements in associative arrays are accessed and manipulated in exactly the same way as normal arrays are - using square braces (`[...]`). In this case, if we wanted to access the value stored under 'Matt', we could type

  `lunches['Matt']`

If we wanted to alter that value, we could perform an assignment, just like we might with a normal array.

  `lunches['Matt'] = 'turkey sandwich'`

Adding new key-value pairs looks just like assignment - you simply set your new key as the reference and assign your new value as the value.

  `lunches['Elena'] = 'meatloaf'

Keys can be strings or numbers (or even another type of data that we haven't talked about, *symbols*), and basically anything can be used as a value (including an array, or even another associative array). Here's an example of all of the above:
```javascript
  var candidate_data = {
    'name' : "John Doe",
    'age' : 32,
    'isFullTime' : true,
    'pastEmployers' : ['Microsoft','Google','Amazon'],
    'yearsExperience' : {
      'ruby' : 3,
      'java' : 6,
      'javascript' : 5
      }
    }
```

### Test Yourself
Consider the following associative array.
```javascript
  var pet = {
    'species' : 'iguana',
    'gender' : 'female',
    'age' : 12,
    'name' : 'Godzilla'
    }
```
What code could we write to perform the following tasks?
* Retrieve the value for 'name' from the associative array.
* Assign the value for 'age' to 13.
* Add a new key 'favoriteFood', with value 'crickets'

---
[Ready for one last quiz?](09_quiz.md)
