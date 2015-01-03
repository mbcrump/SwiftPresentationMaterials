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

Postfix does not increase the value of its operand until after it has been evaluated. 

Prefix decrement increases the value of its operand before it has been evaluated. 

		++count
		count++
		
prefix and posfix example:

	1> var x = 1 
	x: Int = 1
  	2> println(x++) //postfix
	1
  	3> var x = 1 
	x: Int = 1
  	4> println(++x) //prefix 
	2
  	5> var x = 1 
	x: Int = 1
  	6> println(x++) 
	1
  	7> println(x) 
	2
  
Unary Minus Operator is short-hand for multiplying a variable's value by -1. 

	let a = -33
	
##Binary Operators

They are operands, which are values on either side of the operator. 

	a + b
	
a and b are operands and + is the operator. 

##Remainder Operator

Uses the % sign and allows remainders for Double Types unlike C

	int a = 8
	int b = 6
	let c = a % b
	let d = 8.0
	let e = 2.5
	let f = d % e
	
	
##Range Operators
Are denoted by two dots and a left angle bracket or three dots depending on what type of range you need. 

Closed-ranged sample are good for ranges where you want both the first and the last value of the range to be included.  

	for a in 1...5 { println(a) }
1
2
3
4
5

Half-ranged are good for zero-based list such as arrays, where the index of the first element is 0, then 1 and 2. 

	for a in 1..<5 { println(a) } 
1
2
3
4

##Logical Operators
They evaluate and return Boolean value types based on logic. 

###AND 

	let a = true
	let b = false
	let c = a && b

###NOT

It inverts the value of a Boolean variable.

	let a = true
	let b = !a //false now
	
**It must a prefix operator.**

###OR
Evaluates two operands and decides whether one is true or not, no matter which one, and then returns its results. 

	let a = true
	let b = false
	let c = a || b
	
	
##Arrays
Ordered sets of data and every member inside an array must be of the same type. 

Any of the following types produce the same results: 

	let myArray: Array<Int> = [1,2,3]
	let myArray : [Int] = [1,2,3]
	let myArray = [1,2,3]
	
Keep in mind that Array Member Types Cannot change due to type safety. 

You can initialize an empty array with the following:

	var items = [String]()
	
All arrays are zero-based.

Subscripts are indexes enclosed inside square brackets immediately following the name of the array in code. 

###Manipulating Arrays

Here is an example of using subscripts to manipulate an array. 

	var myArray : [String] = ["Foo", "Bar", "Baz"]
	myArray[1] //Bar
	myArray[1] = "Dog"
	myArray[1] //Dog
	
You can add one to it by either of the following ways: 

	myArray.append("Another Dog")
	myArray += ["Cat"]
	
Insert elements into an Array

	myArray.insert("Zero", atIndex :1)
	 
    [0] = "Foo"
    [1] = "Zero"


##Dictionaries

##Tuple
Not a declarable data type like an array, etc... but can be used to get data of varying types from dictionaries and other structures. 

##Contact Info
by: Michael Crump 

[Twitter](http://twitter.com/mbcrump)

[Blog](http://michaelcrump.net)

[About Me](http://about.me/mbcrump)