Java requires a public class FileName to be the name of the actual file in order for it to work. File name usually all caps. Class usually all caps
	`public class FileName{
	`}`
inside the public class File name is the actual program. 

you have your main 
	`public static void main (String[] args){
	`}`
	public allows it to be called 
	static means it does not change 
	void means it returns void. Can be data type if returns value 
	String[] args idk but need them

to get user input
	`import java.util.Scanner`
	`Scanner scan = new Scanner(System.in)`
		This creates a variable of type Scanner and sets it equal to a new scanner that reads the System input 
		reads as a string
		to get value other then string 
		`int userInput = Integer.valueOf(scan.nextLine())`
			This pulls an integer value from 

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
	
	
