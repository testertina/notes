# Javascript 2

## Intro to Control Flow
### If statements and else

Can create if statements to set parameters which can return specific outcomes.

```
var cash = 4;

var cash = prompt("How much money do you have?");

if (cash > 7) {
	console.log("You can drink!");
}	else {
	console.log("Thou shall not drink");
}
```

### If, else if and else

Can use an additional else if statement in between an if and else statement to add more parameters.

```
var cash = prompt("How much money do you have?");

if (cash > 7) {
	console.log("You can drink!");
}	

else if (cash > 5) {
	console.log("You can buy some crisps!");
}

else {
	console.log("Thou shall not drink");
}
```

```

```

### Boolean Operators

To return true when one condition is true use or:

``` || ``` or.

To return true when all conditions are true use:

``` && ``` and.

### Switch Statements

Can use switch statements to return a response when certain cases are met.  Once the case is met the statement will break.

```
switch() {
	case '':

	break;

	case '':

	break;

	case '':

	break;

	default:
}
```

```
var name = "Timmy";

switch(name) {
	case 'Tina':
		console.log("Hello Tina");

	break;

	case 'Bob':
		console.log("Hello Bob!")
	break;

	case 'Sammy':
		console.log("Hello Sammy!")
	break;

	default:
		console.log("Sorry, don't know who you are.")
}

```


### Truthy and Falsey

All values in js have a truthy and falsey element.

## Loops

### For Loops

```
for (var i = 0; i < 10; i++) {

}

```

``` for i = 0; ``` Initialisation.

``` i < 10; ``` Condition to this value.

``` i++ ``` Increment this variable.

Example a function to run on a loop.

```
var people = ["Tina", "Bob", "Simon", "Jeff"];

function greetPeople(listOfPeople) {

	for (var i = 0; i < listOfPeople.length; i++) {
		greet(listOfPeople[i]);
	}
}

function greet (name) {
	console.log("Hello " + name);
	
}

greetPeople(people);
```

### While loops

```
var i = 0;

while (i < 5) {
console.log("Conditions have been met.");
console.log(i);
i++
}

```

Example

```
var isDrunk = false;
var drinks = 0;

while (!isDrunk) {
	console.log("There you go, enjoy your drink.")
	drinks++
	if (drinks === 5) {
		isDrunk = true;
	}
}
```

### Iterating over an object


Define an object.


```

var people = {
	"Niall": "Richmond",
	"Tim": "Newcastle",
	"Bob": "Birmingham"
};
```

Iterate over the object using a for loop, remember we can call the values in an object using the key or object.key call.

```
for (var key in people) {
	console.log("Hello, " + key + ". You live in " + people[key]);
}
```

###  Ternary statements

```
i%15 === 0 ? console.log(“FizzBuzz”) : i%5===0 ? console.log(“Buzz”) : i%3 === 0 ? console.log(“Fizz”) : console.log(i)
```