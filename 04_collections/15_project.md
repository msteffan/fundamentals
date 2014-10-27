**Collections**

---

# Collections - Exercise

## Objectives

* Practice with arrays
* Practice with iteration
* Practice with hashes

Let's apply our newly learned skills to Project Todo. Let's start of by using
an array to manage our todos. Each todo will simply be a string for now (like
"Wash the car").

#### Phase 1

* At the very top of our program, create an array with three todos in it to get
  us started. Store this array in a variable called `todos`.
* When the user selects `1` from the menu, iterate over our `todos` array and
  print each todo.
* When the user selects `2` from the menu, prompt the user to input the content
  for the new todo, and push this string into the `todos` array
* When the user selects `3` from the menu, prompt the user to input an index
  number. Use this index number to delete the corresponding todo in the `todos`
  array. Read [this](http://www.ruby-doc.org/core-2.1.3/Array.html#method-i-delete_at)
  to find out how.

#### Phase 2

Modify your program so that each todo is not a string, but a hash with two
key-value pairs. The first key is `"content"`, and contains the content of the
todo. The second key is `"status"`, and contains a string that is either `"pending"`
or `"done"`. For example,

```
example_todo = {
  "content" => "Build a time machine"
  "status" => "pending"
}

another_todo = {
  "content" => "Scuba dive in a bathtub"
  "status" => "done"
}
```

* When the user selects `1`, each todo should be printed with its status, like
  so.

```
Get a haircut - pending
Watch Breaking Bad - done
Eat ice cream - pending
```

* When the user selects `2`, the user should be prompted for the content of the
  todo, and the newly created todo should have a status of "pending".

* When the user selects `3`, the user should be prompted for the index of the
  todo they wish to complete. Instead of deleting the todo from the array,
  simply change its status to "done"
