## Stuck?

**Spoiler alert!**

Don't look any further unless you're really stuck. If you
hit a problem, or don't remember something, try things! Look it up on the
internet! If you _still_ don't have an answer, then you can use the information
below. Happy coding!

#### Phase 1

```ruby
puts("Welcome to Project Todo")

puts("Menu")
puts("----")
puts("1. View my todos")
puts("2. Add a todo")
puts("3. Complete a todo")
puts("4. Exit")
puts("Enter your choice:")
user_input = gets().chomp().to_i()

puts("The user entered")
puts(user_input)
```

#### Phase 2

```ruby
puts("Welcome to Project Todo")

puts("Menu")
puts("----")
puts("1. View my todos")
puts("2. Add a todo")
puts("3. Complete a todo")
puts("4. Exit")
puts("Enter your choice:")
user_input = gets().chomp().to_i()

puts("The user entered")
puts(user_input)

if user_input == 1
  puts("Under construction. You will be able to view your todos soon!")
elsif user_input == 2
  puts("Under construction. You will be able to add todos soon!")
elsif user_input == 3
  puts("Under construction. You will be able to complete todos soon!")
elsif user_input == 4
  puts("Thank you for using Project Todo. Have a nice day.")
end
```

#### Phase 3

```ruby
puts("Welcome to Project Todo")

while true
  puts("Menu")
  puts("----")
  puts("1. View my todos")
  puts("2. Add a todo")
  puts("3. Complete a todo")
  puts("4. Exit")
  puts("Enter your choice:")
  user_input = gets().chomp().to_i()

  puts("The user entered")
  puts(user_input)

  if user_input == 1
    puts("Under construction. You will be able to view your todos soon!")
  elsif user_input == 2
    puts("Under construction. You will be able to add todos soon!")
  elsif user_input == 3
    puts("Under construction. You will be able to complete todos soon!")
  elsif user_input == 4
    puts("Thank you for using Project Todo. Have a nice day.")
    break
  end
end
```
