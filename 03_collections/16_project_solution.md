## Stuck?

**Spoiler alert!**

Don't look any further unless you're really stuck. If you
hit a problem, or don't remember something, try things! Look it up on the
internet! If you _still_ don't have an answer, then you can use the information
below. Happy coding!

#### Phase 1

```ruby
puts("Welcome to Project Todo")

todos = ["Wash the car", "Feed the dog", "Take over the world"]

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
    index = 0
    while index < todos.count()
      puts(todos[index])
      index = index + 1
    end
  elsif user_input == 2
    puts("Enter new todo:")
    new_todo = gets().chomp()
    todos.push(new_todo)
  elsif user_input == 3
    puts("Enter index of todo that you wish to complete:")
    index = gets().chomp().to_i
    todos.delete_at(index)
  elsif user_input == 4
    puts("Thank you for using Project Todo. Have a nice day.")
    break
  end
end
```

#### Phase 2

```ruby
puts("Welcome to Project Todo")

todos = [
  {
    "content" => "Wash the car" ,
    "status" => "pending"
  },
  {
    "content" => "Feed the dog",
    "status" => "done"
  },
  {
    "content" => "Take over the world",
    "status" => "pending"
  }
]

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
    index = 0
    while index < todos.count()
      todo = todos[index]
      puts(todo["content"] + " - " + todo["status"])
      index = index + 1
    end
  elsif user_input == 2
    puts("Enter new todo:")
    content = gets().chomp()
    new_todo = {
      "content" => content,
      "status" => "pending"
    }
    todos.push(new_todo)
  elsif user_input == 3
    puts("Enter index of todo that you wish to complete:")
    index = gets().chomp().to_i
    todos[index]["status"] = "done"
  elsif user_input == 4
    puts("Thank you for using Project Todo. Have a nice day.")
    break
  end
end
```
