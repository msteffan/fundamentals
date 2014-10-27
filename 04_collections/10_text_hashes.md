**Collections**

---

#### Hashes

Good news! Timmy has a track and field event coming up, and he needs to register for it.
In order to register, he needs to give the organizers his name, age, height, weight,
and event. This is an assortment of pieces of information, and the order of this
information doesn't matter.

If Timmy used an array to pass this information to the organizers, it might look
something like this.

```ruby
["Timmy", 20, 70, 140, "100m sprint"]
```

The problem with using an array for this set of information is that it's not
clear what is what. The organizers might think his name is "100m sprint", and he
wants to participate in the "Timmy" event. They may think he is 140 inches tall (that's
more than 11 feet) and weights 20 pounds!

The underlying problem is that the order of these pieces of information is irrelevant.
What we want to do is give each object inside a label, so that the organizers know what
is what.

A data structure where order doesn't matter, and each object has a label, is
called a hash! Generally, we like to call the labels "keys", and the objects "values".
In this way, a hash can be thought of as a set of "key-value pairs". A bunch of objects,
each with a label.

Hashes in Ruby are created using the following structure.

```
{ key => value, key => value}
```

Hashes in Ruby are represented by putting key-value pairs inside curly braces. Each
key-value pair is separated by commas.

The little arrow pointing from key to value is actually an equal sign and a
greater than sign next to each other. It's commonly called a "hash rocket".

Keys can be any type of data. They can be strings, numbers, booleans, etc. We'll
stick to using strings for now.

**Create**

Let's construct a hash to help Timmy register for his event.

```ruby
registration_info = {
  "name" => "Timmy",
  "age" => 20,
  "height" => 70,
  "weight" => 140,
  "event" => "100m sprint"
}
```

The fact that this hash is spread over multiple lines does not matter, as long as each
key-value pair is still separated by commas.

Great! Now the organizers won't be confused about what is what inside this data
structure. If they want to know the name of the registrant, they can ask the hash for
exactly that piece of information, like so.

```ruby
registration_info["name"]    # This will produce the result "Timmy"
```

When dealing with arrays, we used an index inside square brackets to find an object by
its position. With hashes, we use a key, or label, inside square brackets to find an
object by its key.

When the organizers receive this hash of information from Timmy, they can extract the
information inside like so.

```ruby
name = registration_info["name"]
age = registration_info["age"]
height = registration_info["height"]
weight = registration_info["weight"]
event = registration_info["event"]
```

**Insert**

If Timmy forgot to add his team name to this hash when he created it, he can
add it later like so.

```ruby
registration_info["team_name"] = "Gryffindor"
```

His hash now has the value "Gryffindor" in it, with the label "team_name".

**Modify**

We can modify existing values in a similar way.

```ruby
registration_info["name"] = "Timothy"
```

**Remove**

We can remove values from a hash (along with their associated keys) by using
an ability of hashes called `.delete()`, along with the key whose value we want
to remove.

```ruby
# The organizers don't need to know Timmy's weight
registration_info.delete("weight")
```

Now, the hash does not contain the value 140, nor does it contain the key "weight".
The entire key-value pair has been removed from the hash.

The analogy of Timmy and these organizers is very similar to how forms on the internet
send their information to a server. Timmy is very much like a form on the internet,
and the organizers are like a Rails server. Rails receives and handles information
from a form as a hash to avoid the "what is what" confusion.
