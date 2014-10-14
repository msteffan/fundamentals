# Hashes

Consider the following hash

```ruby
stats = {
  "health" => 100,
  "foods" => ["apple", "cake", "biscuit"],
  "weapon" => "sword",
  "items" => ["torch", "rope", "key", "bucket"]
}
```

Write the code to perform the following actions.

* A zombie slashes you. Reduce your health by 10 points.
* You'd better fight back. Display what weapon you are holding.
* Your sword broke as you slew the zombie. Change your weapon to "staff"
* You eat the last food in your collection of food. Remove it from your foods
  array and increase your health by 5 points
* You approach a locked door. You look through your items to find something
  useful. Display your list of items.
* Your key should work! Use it to open the door! Remove "key" from your items
  and display the mesage "The door opens."
