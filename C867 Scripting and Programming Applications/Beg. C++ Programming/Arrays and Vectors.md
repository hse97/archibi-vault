### Arrays
compound data type or data structure
collection of elements
all elements are of the same type 
each element can be accessed directly 

##### Characteristics
Fixed Size
Elements all same data size
store contiguously in memory 
Individual elements can be accessed in memory by position index

index starts at 0
last index = n - 1

no checking to see if you're out of bounds

Always initialize an array 
Very efficient
Iteration (looping) is often used to process

### Declaring and Initializing Arrays
`element_type array_name [constant number of elements`

`int testScore [100];` // integer array with 100 indexes
`const double hiTemps [testScores]; ` // can be constant, other data types, use a variable as the index parameter

to initialize 
`element_type array_name [number of elements] {init list}`
	`int testScores [3] = {1, 2, 3};`

### Multi-dimensional arrays
`element_type array_name [rows] [cols];`
	`double heightOfMenByAge [10][5]`

### Vectors
dynamicly sized array
saves memory and adapts to the true size of elemens in the array

container in the c++ standard template library
can grow/shrink at execution time
similar syntax as arrays

`#include <vector>` pre-directive needed to use

`vector <char> vowels;`
`vector <int> testScores;`

Declaring Vectors:
`vector <int> testScores (10)` //creates integer vector with pre-set, but still dynamic, size of 10 that is empty 
`vector char letters {'a', 'b', 'c'};`//creates a dyanmic sized char vector with first 3 set
`vector <double> hiTemps (365, 80.0)` //creates a double vector of 365 sized with 80.0 set for all 365 original values

### Accessing and Modifying Vectors
Can access vector elements with array syntax
if you have:
`vector <int> test_scores {100, 95, 99, 87, 88};`
can access it with:
`test_score [1];

better to use vector syntax - using at
`vector_name.at(element_index)`
	`testScores.at(1);`
gives you value at a specific location 

Vectors grow as needed with the pushback feature
`vector_name.push_back(element)`
say you have
`vector <int> test_scores {100, 95, 99};`
	`test_scores.push_back(80)` // 100, 95, 99, 80
can get size with 
`test_scores.size()` to print out literal of vector size







