Object-Oriented means isolating concepts of a problem into separate entities and then using those entities to solve problems 

### Classes and Objects
**Class**
	defines the attributes of an object, information related to them (i.e variables), their commands (methods). 
**Method**
	Piece of source code written inside a class
	has been named
	can be called
	methods are always a part of a class and is often used to modify the internal state of an object instantiated from a class 

and example is `ArrayList` as it is a class offered natively by Java. When creating a specific array list `ArrayList<Integer> integers = new ArrayList<>()` you're creating an object called `integers` and it's created from the class `ArrayList`

### Creating New Class
Create a new file of `.java` with the name of the class 
	to create a class called person 
	create a new file named `Person.java`
	in the new file start the file with `public class Person {
	`}`
variables defined inside the class are called **instance variable**
 instance variables with the keyword **private** means the variables are 'hidden' inside the class
 this is known as **encapsulation**

### Defining a Constructor 
set initial state for created objects
created same way pre-made java classes are made 
	use the `new` keyword
	`Person ada = new Person("Ada");` 
		`Person` defines the object as `Person` class 
		`ada` is the name of the new object created from `Person`
		`new Person("Ada")` is calling the constructor and passing `"Ada"` as a string
 
![[Pasted image 20240726203137.png]]
a constructor is the method that defines the object created 
	constructors name is always the same name as the class 
	constructors set the parameters of the object created, allows for default values to be given at creation, and then modified by the code that is calling the class
		I.g you create a class with the ability to have Name and Score, but upon creation only give it a Name and have the default score to be zero or something 
	the `new Person()` is calling the constructor 
	`this.age = 0` sets the age of the object created (this) to the value of 0
	`this.name = initialName` sets 'this' objects name to name passed as a parameter 
		the constructor is only passed initialName so that is the only dynamic element of the class
		age is hard coded to 0 whenever only a name is passed 

### Default Constructors 
If the program doesn't define a constructor Java builds a default one
default constructors don't do anything apart from creating the object 
objects variables remain uninitiated 
	return `null`
if a constructor is created by the user, calling an empty constructor will result in an error
	if a constructor is defined, creating an object with `Person person = new Person()` will fail unless there is a constructor that accepts no parameters 

### Defining Methods for an Object
Methods are source code inside a class that can be evoked 
	ya know all the `object.doSomething()` things that we're just supposed to know exist 
Methods are written inside the class, below the constructor. 
	constructor must be defined first before method can be called
	`public void methodName(){...}` is an example
		`public` so it can be called from other files/classes/programs 
		`void` as it returns nothing. Can be anything. `int` `String` etc it's a function 

### Changing an Instance Variable's Value in a Method 
you can change initialized values just like any other value. 
`this` keywords refers to the object that is calling the method. `this.age` is just the variable that's calling the method's current set age 
![[Pasted image 20240726213600.png]]
in the example `growOlder()` is just incrementing the object calling `growOlder` value by one 
