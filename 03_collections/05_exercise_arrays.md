**Collections**

---

#### Exercise - Arrays

Given the following list:
```
*nsync
98 degrees
Backstreet Boys
Hanson
O-Town
```

Write a program called `boy_band_tracker.rb`. In this program:

Define a new array and store it in a variable

* Use the `.push()` method to add 1 of the boy bands from the list to your new array
* Add a second band the array without using the `.push()` method

Define a while loop. While the number of boy bands is less than 5, print out a statement asking the user to input another boy band. Add the band entered by the user to the current list. Then:

* Using either the `.first()` method or index values print out the first band in the list
* Using the `.pop()` method remove the last boy band from the list.
* Change the current last boy band from `Hanson` to `Handsome young chaps`

Make a new array called `last_bands_standing`. While the number of boy bands in the array is less than 3:

* remove a boy band from the first array and add it to the new array
* print a statement that says `[BAND] is one of the last bands standing`
