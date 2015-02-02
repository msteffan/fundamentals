**WDI Fundamentals Chapter 6**

---

##Associative Arrays

In the last lesson, we looked at Arrays.  

```js
var basicArray = new Array();
basicArray[0] = "Portland";
basicArray[1] = "Beaverton";
basicArray[2] = "Lake Oswego";
console.log(basicArray.length);
// --> Outputs 3, as expected

var associativeArray = new Array();
associativeArray['city'] = "Portland";
associativeArray['state'] = "Oregon";
associativeArray['country'] = "United States";
console.log(associativeArray.length);
// --> Outputs 0 in Chrome, what the heck?

// we can also access values through .property notation ?!
console.log("City is: " + associativeArray['city']);
console.log("City is: " + associativeArray.city); 

// outputs
// --> City is: Portland
// --> City is: Portland
```





