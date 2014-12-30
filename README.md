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



##Contact Info
by: Michael Crump 

[Twitter](http://twitter.com/mbcrump)

[Blog](http://michaelcrump.net)

[About Me](http://about.me/mbcrump)