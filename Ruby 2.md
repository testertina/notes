# Ruby 2

## Classes

When we create a class we also need a initialise method which is a constructor.  Classes can be used anywhere.

Anything created within the class is an instance of the class. Classes have capital letters in the beginning, CamelCasing.

```
class Phrase
	def initialize
	end
end
```

## Instance variables

Accessing instance variables.

```
class Account
	# Create method called balance that lets me access the balance instance variable.
	attr_accessor :balance

	def initialize balance
		@balance = balance #instance variable: gets attached to the instance account created in app.rb
	end
end
```

attr_accessor will make the instance variable balance available to be read/written to within the class Account.  When being read it will need to be referred to at @balance.  Called in its instance.

With instance variables, you can make them accessible or not with attr_reader and attr_writer outside of the class.

attr_reader will make the instance variable available to read.

attr_writer will make the instance variable available to write to.

