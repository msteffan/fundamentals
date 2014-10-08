**A Computer Program**

---

#### Quiz - Conditionals

What do the following expressions produce?

* 12 > 3
  * true (ANSWER)
  * false
* 9 < 5
  * true
  * false (ANSWER)
* 3 == 4
  * true
  * false (ANSWER)
* 8 != 12
  * true (ANSWER)
  * false

```ruby
puts("How many pushups do you want me to do?")
pushups = gets().chomp().to_i()

if pushups < 10
  puts("Piece of cake, no problem.")
elsif pushups < 20
  puts("I think I broke a sweat.")
elsif pushups < 30
  puts("This is not as easy as I thought, but I can do that.")
else
  puts("Nice try. I'm going to go play video games.")
end
```

* What message will be displayed if the user enters `27`?
  * "Piece of cake, no problem."
  * "I think I broke a sweat."
  * "This is not as easy as I thought, but I can do that." (ANSWER)
  * "Nice try. I'm going to go play video games."
