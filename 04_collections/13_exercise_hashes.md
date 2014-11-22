**Collections**

---

#### Exercise - Hashes

Given the following array:
```
["Thriller", 1982, "Michael Jackson", "Epic Records", ["Wanna Be Startin' Somethin", "Baby Be Mine", "The Girl in My Life"]]
```
Write a program called `thriller.rb`. In this program:

Assign the value above to a new variable called `album_array`
Define a new hash called `album_hash` and initialize it with the following keys (the values of the keys should be set to nil):

```
title
year_released
artist
label
tracks
```
Look at the `.keys()` [method](http://www.ruby-doc.org/core-2.1.2/Hash.html#method-i-keys) available to hashes. What does it return?

Using the `.keys()` method, define a while loop that will iterate over the hash's keys adding the appropriate values to the hash representing the attributes of the Thriller album, copying over the values from the `album_array`.
