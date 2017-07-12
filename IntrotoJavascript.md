# Javascript (mozilla JS reference).

## Languages

* JavaScript (front end)
* nodeJS (backend)
* .net (backend)

Look up ServerSite.

No compiling with JS, it's an interpretive language.

## Writing JS

* Write JS in webdev mode in Chrome browser. 

* Create JS file in terminal using
```
touch main.JS
```.

### Defining variables

To declare a variable use ```var```:

```var myName;```

```myName = "Tina";```

or

```var myName = "Tina";```

Types of variables:

* String
* Number
* Boolean
* Undefined
* Array
* Objects
* NaN
* Null

Print myName variable to the console:

```console.log(myName);```

Convert to upper case:

```console.log(headline.toUpperCase());```

Select a substring of text from a string:

```headline.substr(0, 4);```
This will return the characters between index 0 and 4.

Display alerts in a browser:

```alert(myName);```

To create dates:

``` var dob = new Date("August 4, 1992"); ```

To call today's date:

``` var dob = new Date(); ```


Refresh page to clear var definitions.

## Where to run JS

### The head of a html file.

```
<html>
<head>
	<title>Intro to Javascript</title>
	<script>

		alert("Hello Tina");

	</script>
</head>
```

### The body of a html file (inline).  (BAD PRACTISE)

```
<body>

	<h1>Intro to Javascript</h1>
	<button onclick="alert('Hello Tina')">Click Me!</button>

</body>
```

Above is an example of bad practise code.

### Within the body using an JS file (external). (BEST OPTION)

```
<head>
	<title>Intro to Javascript</title>

		<script src="main.js"></script>
	
</head>
```
Above links the external main.js file to your html file (similar to linking CSS files).  The link means that the JS file will affect the entire HTML document.

The main.js file looks like this:

```
alert("This is the first line of the main.js file.");

console.log("Hello Tina, this is an external JS file.");
```
## Working on the Chrome console

We can create a testing JS file in sources/snippets.  Add a snippets.

## Working with JS

### String concatenation

If we define two variables, myVariable and message.

We can define a new variable concating the two.

```
var headline = myVariable + message;
```

### Numbers and Operators

```
var myNumber = 10;
```

Operators:
```
+, -, /, *, %, ==, ===, <=, >=, !=, !!=
```

```
console.log(myNumber + 3 - 20 * 4);

-67
```

If you tried to multiply a string by a number, the console would return a ```NaN``` rather than throw an error.


Integers: whole numbers.
Floats: decimals.
Boolean: True or False.

### Arrays

We can define an array using:

```
var myArray = ["Hello", true, 0.97, "Tina"];
```

Can use powers to manipulate the array:
```
myArray.length
```

Can call an index from the array:
```
myArray[3];
0.97
```

### Objects

Define an object using:

```
var myObject = {
	key1: "Value1",
	key2: "Value2"
};
```

Can call specific keys or values using:

```
myObject["myName"];
"Tina"
myObject.myName;
"Tina"

myObject.myName = "Not Tina';
"Not Tina"
```

### Undefined and Null

Undefined: Variable which has not been assigned to anything.
Null: Used when we want to set a variable back to nothing.

### Converting from different data types

From string to number:

``` Number(myVariable); ```

or

``` myVariable.spilt(""); ```

or

``` parseInt(myVariable); ```

or

``` parseFloat(myVariable); ```


From number to string:

``` String(myNumber); ```

or

``` myNumber.join(""); ```

## Functions

### Named Function

The function created can be named (in example addTwoNumbers).

``` 
function addTwoNumbers (name) {

   console.log("Hello " + name) 

} 

addTwoNumbers("Tina");
Hello Tina 

```

```

function addTwoNumbers (number1, number2) {
    var result = number1 + number2
    console.log(result)
    
}

addTwoNumbers(34, 8);
42

```

If another function is written with the same named available it will override the old function.

### Annonymous Function (unnamed)

Just stores the value or output of the function in the variable. Does not name the function.

```
var addTwoNumbers = function (number1, number2) {
    var result = number1 + number2
    console.log(result)
}
```

### Return in functions

Using return in a function will store a variable.  At the point of which return is used it will kill the function and nothing written after the return will run.

```
function addNumbers(num1, num2) {
    return num1, num2;
}

var sumOfNumbers = addNumbers(45, 67);
```

Here, the value of the function addNumbers will be stored in sumOfNumbers.  If the var was defined within the curly brackets of the function after the return call, the value would not be stored in the variable sumOfNumbers.

## Global expressions

replace: searches word for specified characters and replaces them with nothing (""). i case insensitive, g is global so it will replace every instance of the the characters to be searched.

```
function stripVowels(word) {
  	var output = word.replace(/[aeiou]/gi, "");
  	return output;
}
```

https://lornajane.net/posts/2011/simple-regular-expressions-by-example