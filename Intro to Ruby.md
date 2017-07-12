# Ruby

## Intro to Ruby

Compiled language, easy to read. No semi-colons. Will not run correctly with poor alignment.

``` irb ``` in terminal will allow you to use Ruby.

Can open a ruby program using ``` ruby programname.rb ```

### Commands

``` puts ``` and ``` print ``` prints string.

``` p ``` will print whatever you've written following.

### Gems

Gems are packages which can be installed and they are stored in a Gem file. (Similar to font awesome packages we may use in JS.  Instead of linking the package using CDN we install the packages on Ruby using Gem).

``` gem install bundler ``` to install bundler package.

``` bundler init ``` create a gemfile.

``` bundler -h ``` will bring up help and explain what the Gem does.

Can write in the gem file what packages we would like to install.

In the gemfile ``` gem 'mac-say' ```

Then in terminal use ``` bundle ``` to run the Gem file.

Within the ruby file, specify the package you want to use, ``` require 'mac/say' ```.

``` 
require 'mac/say'

Mac::Say.say "Hi, This is about as basic as Ruby script can be. Hope you enjoy it. Right, I'm off" 
```
* Mac::Say -->  Using mac say package.
* .say is a method.
* The string is the argument.

## Syntax

Snakecase: lower case words seperated by underscore.

``` my_variable = 5 ``` How to define a variable.

``` puts my_age + 12 ``` uses the add method (it's like my_age.+(12)).

``` .to_int ``` converts to whole number.

``` .to_s ``` converts to string.

``` 
puts my_name.reverse
puts my_name.length
puts my_name.upcase
puts my_name.lowercase
```

Can find all the methods we can use by using ``` .method ```.

Methods ending with ? will return a Boolean.
Methods ending with ! will replace the variable you've defined.

``` 
my_array = [1, 2, 3]
puts array.pop
```
Takes last array value, takes it out of array and return it.

 
``` 
my_array = [1, 2, 3]
puts array.shift
```
Takes first array value, takes it out of array and return it.

```
:balance
```

This is a symbol, which is a variable that cannot be changed.

### Classical inheritance

http://edwinmeyer.com/Release_Integrated_RHG_09_10_2008/images/ch_minimum_classtree.jpg

### String interpolation

``` puts "This is a string with #{my_age} in it" ``` Converts the variable my_age to string.

### Hashes (objects)

Can define hashes in two ways

```
my_hash {
	name: "Tina",
	job: "Trainee",
	age: 24
}

my_second_hash {
	:name => "Tina",
	:job => "Trainee",
	:age => 24
}

```

``` :name ``` is a symbol.

To call a specific key in the hash we use:

``` puts my_hash[:name] ```

### Lab

RSpec is a Behaviour-Driven Development tool for Ruby programmers. BDD is an approach to software development that combines Test-Driven Development, Domain Driven Design, and Acceptance Test-Driven Planning. RSpec helps you do the TDD part of that equation, focusing on the documentation and design aspects of TDD.

``` require_relative ``` complements the builtin method require by allowing you to load a file that is relative to the file containing the ``` require_relative ``` statement.

## Control Flow

### If, elsif, else

```
if x == 10
	puts "hello"
elsif x == 20
	puts "old"
else
	puts "Goodbye"
end
```

### If, elsif, else, then

```
val = 1

if (val == 1) then puts "1" else puts "not 1" end
```
### Ternary operator

```
x = 10

puts x < 10 ? "it is greater" : "not greater"

```

Every object is false in Ruby until it is defined otherwise.

### And/Or

```
x = 5
y = 10

if x == 5 and y == 9 
	puts "correct"
end
```
This prints nothing to the terminal and it is not true. Can also use &&.

```
x = 5
y = 10

if x == 5 or y == 9 
	puts "correct"
end
```
Can also use ||.

### Gets

```
puts "What is your name?"
x = gets.chomp

puts x

```
