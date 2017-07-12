# Javascript Scope

## Intro to JS scope

### Global Scope

Everything within the main js file.  Anything/one can use this.

```
var name = "Tina"; 

function sayHello () {
	console.log(name)
}
```

Global scope variable and global scope function.

### Lexial Scope

An element that has been defined within a function or lexial scope.

```
function greetPerson () {
	var name = "Simon";
}

greetPerson();

console.log(name);
```

Here is a variable, name, that has only been defined in the function greetPerson, therefore it cannot be called outside of the function.

```
function firstFunction () {
	console.log("I am the first function.");
}

function secondFunction () {
	firstFunction();
	console.log("I am the second function");
}

```

The first function here will be called if the second function is called as the first function is a global function.

### Nested Lexial Scope

```
function firstFunction () {
	console.log("I am the first function.");


	function secondFunction () {
		firstFunction();
		console.log("I am the second function");
	}

}

firstFunction();
secondFunction();

```

Above we have the second function defined within the lexial scope of the first function.  Therefore when the seond function is called in the global scope there is a error explaining that the second function is not defined.  But the first function will work when called in the global scope as it is defined in the global scope.

```
function firstFunction () {
	console.log("I am the first function.");


	function secondFunction () {
		console.log("I am the second function");
	}
	secondFunction();

}

firstFunction();

```

Above there is a nested function (second function) in the scope of the first function. Calling functions in the above manner will allow both to run.

### Debugging

Use the word debugger to make variables known to you.

```
var name = "Tina";

function createVariables () {
	var hairColour = "Black"
	debugger
}

createVariables();
```

we can call haircolour in the console due to the debugger keyword.

### Scope Quirk

```
var name = "Tina";

function createVariables () {
	hairColour = "Black"
	
}

createVariables();
```

Here, hair colour will still be called in the global scope as it is not defined as a variable. Doing variableName = "Something" overrides everything.

## The DOM and JS

Can call html document to Chrome console screen using:
```
console.log(document.body)
```

### Selector APIs

Can use a call to extract data from the html file.
```
console.log(document.body.children[0].innerHTML)
```

```
.children[]
``` 
Above creates an array from all the elements within the body of the html file.  We can decide which element to call by defining the array index. innerHTML prints the value of the array index to the console.

Can change array values in the html file.

```
document.body.children[0].innerHTML = "Hello Tina"
```
```
var liElements = document.getElementsByTagName("li")

console.log(liElements)
```
```
var selectedElements = document.getElementsByClassName("selected")

console.log(selectedElements)

```
```
var wrapper = document.getElementById("wrapper")

console.log(wrapper)

```

### Web APIs

Can use API to style the HTML.
```
wrapper.style.backgroundColor = "blue";
```

Gives a background color of blue to the div wrapper.

We can use for loops to interate over list items to format multiple elements.
```
var selectedLis = document.querySelectorAll("li.selected")
console.log(selectedLis)

for (var i=0; i<selectedLis.length; i++) {

    selectedLis[i].style.color="red";
}
```

We can also use js to create new elements in our html.

```
var newElement = document.createElement("p")

newElement.innerHTML = "Hi I am new here, can you show me around?"

document.body.appendChild(newElement)
```

## DOM events
