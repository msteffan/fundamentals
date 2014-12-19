**A Computer Program**

#### Quiz - Conditionals

---

You'll need to refer to the code below while taking this quiz. [Click here](https://wdi.typeform.com/to/VhbEim) to take the quiz.

**Reference: Code Snippet 1**

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
