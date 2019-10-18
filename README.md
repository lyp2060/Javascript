# Javascript

## embeded an aleart in the page
```javascript
<!DOCTYPE html>
<html>
<body>

<h2>My First Web Page</h2>
<p>My first paragraph.</p>

<script>
window.alert(5 + 16);
</script>

</body>
</html> 
```

## statement: javascript is case sensitive, sepereated by ; one line can have multiple assigments
```javascript
<script>
var x, y, z;  // Declare 3 variables
x = 5;    // Assign the value 5 to x
y = 6;    // Assign the value 6 to y
z = x + y;  // Assign the sum of x and y to z

document.getElementById("demo").innerHTML =
"The value of z is " + z + ".";
</script>

// put numbers
<script>
document.getElementById("demo").innerHTML = 10.50;
</script>

//declar an object
var person = {
  firstName : "John",
  lastName  : "Doe",
  age     : 50,
  eyeColor  : "blue"
};

document.getElementById("demo").innerHTML =
person.firstName + " is " + person.age + " years old.

// access use []

person["firstName"] + " " + person["lastName"];


// find the type of var

typeof 0 + "<br>" +
typeof 314 + "<br>" +
typeof 3.14 + "<br>" +


//function with argument

<script>
function myFunction(name,job) {
  document.getElementById("demo").innerHTML = "Welcome " + name + ", the " + job + ".";
}

//function call without () will give function definition instead of function result 

<script>
function toCelsius(f) {
  return (5/9) * (f-32);
}
document.getElementById("demo").innerHTML = toCelsius;
</script>

// adding one line below the button
<button onclick="document.getElementById('demo').innerHTML=Date()">The time is?</button>

//change current button content
<button onclick="this.innerHTML=Date()">The time is?</button>

// backslash quote before quote show quote only 

var x = 'It\'s alright';
var y = "We are the so-called \"Vikings\" from the north.";

// following example will return 7

<script>
var str = "Please locate where 'locate' occurs!";
var pos = str.indexOf("locate");
document.getElementById("demo").innerHTML = pos;
</script>

// global match, will show ain,ain,ain

<script>
function myFunction() {
  var str = "The rain in SPAIN stays mainly in the plain"; 
  var res = str.match(/ain/g);
  document.getElementById("demo").innerHTML = res;
}
</script>

// replace from Microsoft to W3Schools

var txt = str.replace("Microsoft","W3Schools");
// to upper or lower
text.toUpperCase()
text.toLowerCase();

//split the array

<script>
function myFunction() {
  var str = "a,b,c,d,e,f";
  var arr = str.split(",");
  document.getElementById("demo").innerHTML = arr[0];
}
</script>

// javascript will convert the strings to number if substrate, multiple or divide, but + will concat them as a string 

// The isNaN() function determines whether a value is an illegal number (Not-a-Number).

// Infinity is a number which is very big, var a = Infinity;

// toString() converts a number to a string 
// valueOf() returns a number as a number, var x = 123, x.valueOf()
// toFixed(10), round a number to fixed 10 digits after .

// toPrecision(4), fixed total 4 digits, including both before and after .

// Number() converts variables to numbers 
// parseInt('10'), converts strings to int 
// parseFloat('10.33) converts string to float 

// var X = Number.MAX_VALUE;
// var X = Number.MIN_VALUE;

// Math
Math.PI
Math.round()
Math.pow(x,y)
Math.sqrt(x)
Math.abs(x)
Math.ceil(x)
Math.floor(x)
Math.sin(x)
Math.cos(x)
Math.max()
Math.min()
Math.random(); // return a random number betweeo 0(included) and 1 (excluded)

// Dates
Date(); // display today's date and time 
getFullYear(); // display the year
getTime(); // calculate the number of milliseconds since 1970
setFullYear(); // select a specific date

var d = new Date();
d.setFullYear(2020)

//Array
var cars = ['Saab', 'Volvo', 'BMW']
// or 
var cars  = [
'Saab',
'Volvo',
'BMW'
];

// cars[0] will show 'Saab'

// find the length 
cars.length

// loop thru the whole array

for (i = 0; i<fLen; i++) {
  text += '<li>' + fruits[i] + '</li>'
}
</script>

// adding an element to arr
fruits[fruits.length] = 'Lemon

// if fruits[index] the index more than the fruits.length, there will be some undefined value in between 

fruits instanceof Array; //will return true
// or 
Array.isArray(fruits)

// push() method will append a new element in the end of the array
fruits.push('kiwi')
fruits.pop()
fruits.join('*')


// concat to merge two arrays
var myGirls = ["Cecilie", "Lone"];
var myBoys = ["Emil", "Tobias", "Linus"];
var myChildren = myGirls.concat(myBoys);

//concat three arrays

var arr1 = ["Cecilie", "Lone"];
var arr2 = ["Emil", "Tobias", "Linus"];
var arr3 = ["Robin", "Morgan"];

var myChildren = arr1.concat(arr2, arr3); 
// slice, create a new array by get array[start] and array[end] but not inlcude array[end], orignal array will not touch 
array.slice(start, end)

// kyes() return a new Array Iterator object that contains the keys for each

arr.keys()
arr.shift(); // remove the first element and remove it, it will change the length of the arr
arr.unshift(4,5); // add 4,5 in the begining of the arr
arr.short(); // sorts the elements of an array in place and returns the sorted array 
arr.toString(); // returns an array as a comma seperated string 
arr.reverse(); //reverse it 
arr.sort(function(a,b) {return a-b}); // doindg the number sorting 

// forEach 

var txt = "";
var numbers = [45, 4, 9, 16, 25];
numbers.forEach(myFunction);
document.getElementById("demo").innerHTML = txt;

function myFunction(value, index, array) {
  txt = txt + index+ "<br>"; 
}

// will output 0,1,2,3,4
```

### javascript conditions

```javascript 

// if 
if (new Date().getHours() < 18) {
  document.getElementById("demo").innerHTML = "Good day!";
}

if (hour < 18) {
    greeting = "Good day";
  } else {
    greeting = "Good evening";
  }
   
// if , else if and else 
if (time < 10) {
    greeting = "Good morning";
  } else if (time < 20) {
    greeting = "Good day";
  } else {
    greeting = "Good evening";
  }
  document.getElementById("demo").innerHTML = greeting;
 
// switch statement

var day;
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case  6:
    day = "Saturday";
}

```

## for loop etc

```javascript

var text = "";
var i;
for (i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}
document.getElementById("demo").innerHTML = text;


```


