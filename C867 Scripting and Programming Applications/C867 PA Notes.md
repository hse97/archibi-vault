### Step C: Define an Enumerated Data Type DegreeProgram 
enums are user defined types in c++ 
	consist of a set of named integral constants 
	lets you work with set constants rather then random numbers

```
#pragma once
enum DegreeProgram {
SECURITY,
NETWORK,
SOFTWARE
}
```

This is now a data type like int or string that takes only values SECURITY, NETWORK, SOFTWARE, etc 

We can assign other objects this enum 

anytime a file needs to use this enum it must have `#include "degree.h"` in it 

### Step D.1 Create Student Class
To create a class in C++ you split it into two files, the header and the source file 
in this case 
`student.h` 
	header file where you declare the class and its members 
`student.cpp`
	source file where you define the class's member functions

### Step D.2, Getters/Setters/Constructor/Print 
##### Create Accessors (Gettors)
Accessors/Getters allow external code to read the values of private member variables 
Encapsulation protects integrity of data by preventing direct access 
Ex Accessor Function in header file  
	`string getStudentID();`
Ex Accessor Function in cpp file 
	`string Student::getStudentID() {return studentID;}`
##### Create Mutators (Setters)
Mutators/Setters allow external code to modify the value of private variables 
	prevents unauthorized modifications of member variables 
	ensures that changes to data follow certain rules 
Ex setter function in a .h file 
	`void setStudentID(string studentID);`
Ex setter function in .cpp file 
	`void Student::setStudentID(string studentID) {this->studentID = studentID}`
the `this->` pointer used to distinguish between member variables and parameters with same name 

##### Implement Constructor 
Constructors initialize all member variables using the input parameters provided 
sets all member variables to a set known value 
Constructor in Header file example:
```
public:

//constructor

Student(

string studentID,

string firstName,

string lastName,

string emailAddress,

int age,

int daysInCourse[],

DegreeProgram degreeProgram

);
```

Constructor in Cpp file example:
```
Student::Student(

string studentID,

string firstName,

string lastName,

string emailAddress,

int age,

int daysInCourse[],

DegreeProgram degreProgram

){

this->studentID = studentID;

this->firstName = firstName;

this->lastName = lastName;

this->emailAddress = emailAddress;

this->age = age;

for (int i = 0; i < 5; i++){

this->daysInCourse[i] = daysInCourse[i];

}

this->degreeProgram = degreeProgram;

}
```

### Create classRosterArray/ array of pointers 
array of pointers will hold student objects 
array of pointers allows management of Student objects dynamically 
	can create/destroy Student objects at runtime
the header file you just create the blueprint 
	`Student* classRosterArray[5]`
		creates an array filled with pointers that point towards Student 

Have to crate a constructor and destructor for the classRosterArray pointer array 
in the header file it's easy 
`Roster();`
`~Roster();`

in the cpp file you need to initialize all with null pointers then at the end clear and replace with null pointers 
```
//constructor 
Roster::Roster(){
	for (int i = 0; i < 5; i++){
		classRosterArray[i] = nullptr;	
	}
}
```
this creates an array of pointers 5 in size that are set to null

at the end of the program create a destructor 
```
//destructor
Roster::~Roster(){
	for (int i = 0; i < 5; i++){
		delete classRosterArry[i];
		classRosterArray[i] = nullptr;
	}
}
```

This manages the collection of students dynamically 
practices object oriented design principles like encapsulation 

### E.2 Creating a Student Obj from data and populating the classRosterArray
taking each string from studentData and extracting the individual data 
creating a Student Obj using the extracted data 
Add each Student Obj created into the classRosterArray
	store with pointers 

