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

bubble sort 
	`int bubble = array[firstValue];`
	`array[firstValue] = array[secondValue];`
	`array[secondValue] = bubble;`
