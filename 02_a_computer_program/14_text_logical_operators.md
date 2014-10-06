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

The AND operator, represented by `&&` will produce `true` only if both the
conditions on the left and right of the operator are true. If either one of them
is false, or if both are false, the result will be `false`. Hence, the only time
that we will see the message to drive the car is when bothe `seatbelt_on` and
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
