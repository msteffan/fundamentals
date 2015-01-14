**A Computer Program**

---

#### Logical operators

Logical operations allow us to combine multiple conditions into a single Boolean
`true` or `false` result. Consider the following example.

You should drive your car only if your seatbelt is on and your car is started.
The combination of two conditions (your seatbelt situation and your car started
situation) through the AND operation result in a single condition that
represents whether or not you should drive your car. To write this
programmatically,

```ruby
if seatbelt_on && car_started
  puts("We can drive the car!")
end
```

The AND operator, represented by `&&`, will produce `true` only if both the
conditions on the left and right of the operator are true. If either one of them
is false, or if both are false, the result will be `false`. Hence, the only time
that we will see the message to drive the car is when both `seatbelt_on` and
`car_started` are true.

Sometimes, we want to execute some code if either of two conditions is true. For
example, if you are driving your car, you should make a pitstop if you're either
feeling sleepy or feeling hungry (you should definitely make a pitstop if you're
feeling both). This can be represented by an OR operation.

```ruby
if sleepy || hungry
  puts("Time for a pitstop.")
end
```

The OR operator, represented by `||` will produce `true` if either of the two
conditions on the left and right of the operator are true, and also if both
conditions are true. The OR operator will produce `false` only if both
conditions are false.

The NOT operator, represented by `!` works on only one condition, and its job is
to "opposite" whatever it is working on. In other words, the NOT operator will
produce `true` if the condition it works on is false, and will produce `false`
if the condition it works on is true.

For example, when you're driving (yes, you're still driving) you should switch
lanes if nobody is next to you. To write this programmatically,

```ruby
if !car_next_to_you
  puts("Switching lanes.")
end
```

One other concept that comes into play when dealing with logical operators is the concept of grouping. As you've already seen, there are a number of cases when we use parentheses `()` in Ruby, such as when you're calling a method in Ruby, like `puts()`. Another time we use parentheses is when we want to dictate the order of operations among mathematical operators. We are already familiar with this from elementary math – for example, take the simple math problem `(5 + 3) * 2`. We can also do this for logical operators.

For example, what if you want to get an alert to clean up your house only if the house is dirty and either someone is coming over or if there are roaches.

We could write something like this:
```ruby
if house_is_dirty && (friend_visiting_today || roaches_are_present)
  puts("Need to clean up my house!")
end
```

If we didn't add the parentheses in the conditional above, we'd get the wrong results.

Without the parentheses, the conditional would look like this:
```ruby
if house_is_dirty && friend_visiting_today || roaches_are_present
```

Because we evaluate logical operators from left to right, the conditional would evaluate to true if:
- both `house_is_dirty` and `friend_visiting_today` are equal to true, *or*
- `roaches_are_present` is equal to true

*That's not what we wanted.*

Since we work from left to right, you might think we could fix this by just flipping the operations so that we first evaluate the `||` and then the `&&`, like this:
```ruby
if friend_visiting_today || roaches_are_present && house_is_dirty
```

This doesn't work, though. This is because there is an order of operations for logical operators, just like there is for mathematical ones. When evaluating a mathematical expression, we move from left to right to do all of the multiplication and division first, then go back and do addition and subtraction, right?

In the same way, Ruby evaluates all `&&`s first, before `||`s... **unless you use parentheses to specify an alternative order of operations**.
