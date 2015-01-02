#Swift Presentation Materials
================

##Presentation Outline
###Getting Started
You will need to download Xcode 6 from the AppStore. 
Mac OS X 10.9.3 is the minimum version to run Xcode 6.


###Exploring the IDE
Create a new project and navigate around it. 
Take a look at a playground. 

Mac Playgrounds use

	import Cocoa
	
whereas iOS Playgrounds use

	import UIKit
	
Test out a playground by typing in the following:

	var str = "Hello, playground
	let myNewValue = 40 + 2
	println("My new value is \(myNewValue).")

###Swift Read-Eval-Print-Loop (REPL)
Swift also comes packaged with a nice feature called a Read-Eval-Print-Loop, or a REPL for short.

Open a terminal prompt and enter: 

	xcrun swift

Enter the following code:

	let first = "Hello"
	let second = "Conference"
	let combined = first + second
	
We can also pull in other libraries such as Cocoa with: 

	import Cocoa
	var name = "MICHAEL"
	var lowercase = name.lowercaseString 

You can use :q to quit the terminal. 

##Type Inference

Allows us to not have to explicitly specify the type of variables

For example: 
	
	let myValue = 30 + 2
	
We can assume this will be an Int.

We can declare it as an Int with the following: 

	let myValue: Int = 30 + 2
	
Unsigned Integers which cannot have a negative number, but can hold a large positive number. 

*NOTE* Data Types Cannot Be Changed Once Assigned

Swift prefers Int and Double types. 


##Casting

	let myInt = 5
	let myDouble = Double(myInt)

We could also add to the double. 

##Finding Methods and Properties using Playgrounds

Type the following code: 

	let myInt: Int = 5
	
Hold control key and click Int, this will allow you to find properties and methods. Go ahead and search for description, then hit the back button and type: 

	myInt.description
	
and you will see "5"

##String Interpolation

String interpolation allows you to insert the values directly inline in a string literal, by typing the \ (backslash) key, and then surrounding the value with parentheses.

	let year = 2015
	let currentYearText = "The current year is \(year)"

##Optional Values
Optional Values are declared with a question mark. 

	var myOptIn : Int?
	
The value of myOptIn is nil.

##UnWrapping Optionals
Are there in case a variable may have a value or it may not. The exclamation point ! in the sample below shows an example of this: 

	let degrees = "80"
	let degreesInt = degrees.toInt()!
	
##Optionals
Swift has a concept called optionals, where a variable may have a value, or it may not. In that case, to remain safe from runtime errors.

##Unary

Operates on a single value. They can be a prefix or postfix, meaning they can come before or after a constant or variable. 

		++count
		count++
		
prefix and posfix example:

	1> var x = 1 
	x: Int = 1
  	2> println(x++) 
	1
  	3> var x = 1 
	x: Int = 1
  	4> println(++x) 
	2
  	5> var x = 1 
	x: Int = 1
  	6> println(x++) 
	1
  	7> println(x) 
	2
  

##Logical NOT Operator

It inverts the value of a Boolean variable.

	let a = true
	let b = !a //false now


##Contact Info
by: Michael Crump 

[Twitter](http://twitter.com/mbcrump)

[Blog](http://michaelcrump.net)

[About Me](http://about.me/mbcrump)