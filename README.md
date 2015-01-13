#Learning Swift 
================

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
    
    myArray[3] = "Test!"
    
 Removing items in an araray
 
 	myArray.removeAtIndex(0)
 	myArray.removeLast()
 	myArray = [] //would remove all items
 	
 ###Useful Methods and Properties
 
 	myArray.count
 	myArray.isEmpty
 	myArray.reverse
 	
##Dictionaries

Are similar to arrays in that they hold list of data, except dictionaries are unordered list and instead of accessing them via indexes, dictionary values are accessed via keys. 

	var myDict: Dictionary<String, Double> = ["pi" : 3.14]
	
You can declare a dictionary and initialize it with nothing as shown below: 

	var MyDict =  Dictionary<String, Double>() 
	
Swift can also use type inference to determine which type a variable is:

	var MyDict = ["pi" : 3.14]
	MyDict["pi"] = 4.0 //Updates the value
	MyDict(125,  forKey:"pi")
	MyDict["pi"] = nil // allows you to remove the pair
	
###Useful Methods and Properties
 
 	MyDict.count
 	MyDict.keys
 	MyDict.values

##Tuple
Tuples can be used to extract the index and value from an Array item, or the key and value from a Dictionary item, as a pair that can extract those values to individual temporary values. They are often used in for-in loops 

##Optionals
Optionals in Swift are a way to handle the absence of a value, which can and happens often. 

Optionals only apply to variables and are used by simply adding a ? mark character at the end.

	var myString: String?
	
##UnWrapping
You can unwrap an optional by simply using the ! operator. 

 	1> var optStr: String?
	optStr: String? = nil
  	2> optStr = "Test"
 	3> optStr
	$R0: String? = "Test"
 	4> let unwrappedString  = optStr!
	unwrappedString: String = "Test"
   
Here we can see that we wrapped optStr into a String optional. We used the ? mark to unwrap it into a string and displayed what type of variable it contained. 

**Don't unwrap a nil value**

You can use the if let keyword to see if a value is wrapped or not. This will prevent against hitting nil. 

		if let unwrappedString = optionalString 
		{ println("unwrappedString is not nil, and equals \(unwrappedString)")
		} else 
		{ println("optionalString contains nil")
		}

##Implicitely Unwrapped Variables
These variables are initialized with a value and cannot be nil. 

	var myVar = Int!
	
##Nil Coalescing Operator

	let result = optionalString ?? "No Value"
	
If optionalString is nil, then "No Value" is assigned to result. Otherwise, the unwrapped optionalString value is assigned to result. 

##Understanding nil
Objective-C = uses nil with pointer to an object that does not exist.

Swift = uses nil and it simply means that a value of a certain type is missing. A nil optional that is forced unwrapped will not give a compile-time error. 

##Conditions
Swift contains two conditions : if and the switch statement. 

###If

	let valueToCheck = true
	if valueToCheck {
	// true
	} else {
	// false
	}

the else if gives you additional paths

A full example is shown below: 

	import UIKit
	import Foundation

	let randomNumber = arc4random() % 10
	var result: String!

	if randomNumber == 0 {
    result = "Zero is the first index in an array"
	}
	else if randomNumber == 1 {
    result = "One is the loneliest number..."
	}
	else {
    result = "Our random number is \(result)"
	}	

###Ternary Conditional Operators
It is written as a short-hand for a longer if-else expression that checks a particular case or condition and provides a value for the true branch and another value for the false branch. 

	let value = true
	let a = 100
	let b = 200
	var totalPay = 0

	totalPay = (value) ? a + b : a // 300
	
	//if value was switch to false it would be 100

Remember that parentheses are optional in if statements

###Switch

Like most languages, switch statements must be exhaustive, meaning that you must either provide a case clause and a block of code to execute for every value or provide a default case. 

	let a = 101
	var result : String!

	switch a {
	case 10:
    	result = "a = 10"
	case 100:
    	result = "a = 100"
	default:
    	result = "Does not match either 10 or 100"
	}
	
The result variable would contain the 'does not match either 10 or 100'

Swift does not require an explicit break command at the end of every case block. 

You can also use multiple values in a single case

	let a = 12
	var result : String!

	switch a {
	case 10...12:
    result = "a = 10"
	case 100:
    result = "a = 100"
	default:
    result = "Does not match either 10 or 100"
	}

Wildcards are denoted by the understore _ means that any value in the considered value is a match for that place in the tuple. 

###Switch Tuple Matching

	let e = (302, "Found")
	switch e {
	case (200, _):
    println("success")
	case (302, _):
    println("found")
	case (404, _):
    println("not found")
	default:
    println("server error")
	}

The following will result in nothing matching and the default case working. 

	let e = (302, "Found")
	switch e {
	case (200, _):
    println("success")
	case (302, "willnotmatch"):
    println("found")
	case (404, _):
    println("not found")
	default:
    println("server error")
	}

You can use the where statement to refine the condition to be validated. 

	let e = (302, "Found")
	switch e {
	case (200, _):
    println("success")
	case let (number, word) where number == 302:
    println("found")
	default:
    println("server error")
	}

	//found is printed
	
In Swift, break is implied after each case statement's code has executed. 

Use fallthrough to execute the next case or the default case, whichever may happen first. 

	let e = (302, "Found")
	switch e {
	case (200, _):
    println("success")
	case let (number, word) where number == 302:
    println("found")
    fallthrough
	default:
    println("server error")
	}
	
	//prints found and server error
	

##Contact Info
by: Michael Crump 

[Twitter](http://twitter.com/mbcrump)

[Blog](http://michaelcrump.net)

[About Me](http://about.me/mbcrump)