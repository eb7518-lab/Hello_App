HelloApp Use Case Documentation



This document describes the use cases implemented in the HelloApp project.

The application evolves from a simple console output to a modular application capable of handling multiple inputs, storing names, and displaying formatted greetings.



\---



UC1 – Display Hello World



Description



This use case prints a simple greeting message "Hello World" to the console.

It confirms that the Java environment and Maven project are correctly configured.



Disadvantages of Previous Use Case



No previous use case exists since this is the first implementation.



Preconditions



\- Java installed

\- Maven installed

\- Project structure created

\- HelloApp.java file exists



Main Flow



1\. The application starts.

2\. The JVM loads the HelloApp class.

3\. The "main()" method executes.

4\. The program prints Hello World in the console.



Post Conditions



The console displays the greeting message.



Hints



\- Every Java application starts from the "main()" method.

\- "System.out.println()" prints text to the console.



Code Snippet



public class HelloApp {

&#x20;   public static void main(String\[] args) {

&#x20;       System.out.println("Hello World");

&#x20;   }

}



Concepts Learned



\- Java program structure

\- Console output

\- Main method execution



\---



UC2 – Display User Name from Command Line



Description



The program accepts a single name as a command-line argument and prints a greeting message.



Disadvantages of Previous Use Case



UC1 could only print a fixed message and did not support user input.



Preconditions



\- Program executed with a command-line argument.



Main Flow



1\. User runs the program with a name argument.

2\. The program reads the argument from "args\[]".

3\. It prints a greeting message.



Post Conditions



The console displays Hello <Name>.



Code Snippet



public class HelloApp {

&#x20;   public static void main(String\[] args) {

&#x20;       System.out.println("Hello " + args\[0]);

&#x20;   }

}



Concepts Learned



\- Command-line arguments

\- String concatenation



\---



UC3 – Optional Argument Handling



Description



If the user does not provide a name, the program prints a default greeting.



Disadvantages of Previous Use Case



UC2 fails if no argument is passed.



Preconditions



Program must check if arguments exist.



Main Flow



1\. Program checks argument length.

2\. If no argument exists, print default greeting.



Post Conditions



Program runs successfully with or without arguments.



Code Snippet



if(args.length == 0){

&#x20;   System.out.println("Hello User");

} else {

&#x20;   System.out.println("Hello " + args\[0]);

}



Concepts Learned



\- Conditional statements

\- Argument validation



\---



UC4 – Multiple Command-Line Names



Description



Allows greeting multiple users passed via command line.



Disadvantages of Previous Use Case



UC3 supports only one name.



Preconditions



Multiple arguments passed during execution.



Main Flow



1\. Program loops through arguments.

2\. Each name receives a greeting.



Post Conditions



Multiple greetings displayed.



Code Snippet



for(String name : args){

&#x20;   System.out.println("Hello " + name);

}



Concepts Learned



\- Loops

\- Arrays



\---



UC5 – Read Name from Standard Input



Description



Accepts a name from the keyboard using Scanner.



Disadvantages of Previous Use Case



Previous cases only used command-line arguments.



Preconditions



Scanner library imported.



Main Flow



1\. Program prompts user for input.

2\. User enters name.

3\. Program prints greeting.



Code Snippet



Scanner sc = new Scanner(System.in);

System.out.print("Enter name: ");

String name = sc.nextLine();

System.out.println("Hello " + name);



Concepts Learned



\- Scanner class

\- User input



\---



UC6 – Read Multiple Names from Input



Description



Allows users to enter multiple names interactively.



Disadvantages of Previous Use Case



UC5 allowed only one input.



Main Flow



1\. Program asks for multiple names.

2\. User enters names in loop.

3\. Program prints greeting for each.



Concepts Learned



\- Loops with input

\- Dynamic user interaction



\---



UC7 – Store Names in Collection



Description



Names entered by users are stored in a List collection.



Disadvantages of Previous Use Case



Names were not stored.



Main Flow



1\. Create a list.

2\. Store entered names.

3\. Display stored names.



Code Snippet



List<String> names = new ArrayList<>();

names.add("John");

names.add("Alice");



Concepts Learned



\- Collections

\- ArrayList



\---



UC8 – Remove Names from Collection



Description



Users can remove names from the stored list.



Disadvantages of Previous Use Case



UC7 allowed only storing and listing names.



Main Flow



1\. User selects a name to remove.

2\. Program deletes the name.



Code Snippet



names.remove("John");



Concepts Learned



\- List manipulation



\---



UC9 – Refactor Input Processing



Description



Code is organized into separate methods for better readability.



Disadvantages of Previous Use Case



Code became lengthy and harder to maintain.



Concepts Learned



\- Methods

\- Code modularity



\---



UC10 – Create Name Manager Class



Description



Name management logic is moved into a separate class.



Disadvantages of Previous Use Case



All logic existed in one class.



Concepts Learned



\- Object-oriented design

\- Classes and objects



\---



UC11 – Persist Names Across Runs



Description



Names are saved to a file so that they remain available when the program runs again.



Disadvantages of Previous Use Case



Stored names were lost after program termination.



Concepts Learned



\- File handling

\- Data persistence



\---



UC12 – Display Names in Banner Format



Description



The application displays greetings in a banner-style output for improved visual presentation.



Example:



\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

\* Hello John \*

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*



Concepts Learned



\- Output formatting

\- Enhanced console display



\---



Conclusion



The HelloApp project demonstrates the evolution of a simple Java program into a structured application that supports user input, collections, modular design, persistence, and formatted output.

