to use arrays and lists 
`import java.util.ArrayList;`
`ArrayList<Type> list = new ArrayLIst<>();`
	where Type is the type of value to be stored e.g string
	to get the value from a list you gotta use the `.get(X)` command
		`list.get(9)` to get the 10th value
	to get the size of an array/list use the `.size()` command 
		`list.size()` ouputs # of indices in int format 
	to print the last value any given array/list use 
		`System.out.println(list.get(list.size()-1));`
			`.get() ` to grab the value 
			`list.size() - 1` is the value it gets the size of the array - 1 since index starts at 0
	

To remove values from a list 
	`list.remove(x)` where x is the index location of the value that will be removed

to check the existence of a value in a list 
	`list.contains("Example")` where Example is a string and thus will check for the string 'Example' in the list

to make sure that a list is not empty
	`list.isEmpty()` outputs a boolean true/false if empty or has value. 

Lists as Method Parameters
	`public static void print(ArrayList<String> list)`
		this is a public function that is static, returns void, called print
		its parameter is `ArrayList<String> list` meaning it takes an ArrayList of type String and it will be called list in the function
	`for (String value: list)`
		enhanced for loop or for-each loop
		this for loop defines a String value variable that holds the literal data at each index in the list. It is an easier way to iterate through data held in a index. Cuts down the middle man and you can iterate over a list while using the data literal held by the list
			`System.out.println(value)` 
				This would output ever String value in the list 
	`public static void printSmallerThan(ArrayList<Integer> numbers, int threshold) {
	`for (int number: numbers){
	`    if (number < threshold) {
	`        System.out.println(number);`
	`     }
	`  }`
	`}`
	this function gets passed an ArrayList that holds integers called numbers, and an integer. It iterates through the literal values of the List called numbers. The result is it prints every value in numbers that is < the threshold value. 


reference variables are variables that point to a reference in memory. i.e the variables do not store any information, they store the location of information. 
A list is a reference-type variable. 
When reference-type variables are passed to a method, the method is able to edit the data at this location which in turn edits the data for the original place. 
So the program that calls the method and the method are both referring to the same data at the same location it is not confined to the scope of either 
