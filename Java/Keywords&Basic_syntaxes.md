
1. Imagine there is a file called Main.java, the file name indicates that it contains a class named "Main" inside it. And remember that it is always recommended to put the first letter of the class name in capital letter. If there is no class called "Main" inside Main.java, then we will not be able to run the code.

2. consider the below example,
```java
public class Main{

}
```
In this above code there is a keyword called "public". this keyword is called as access modifiers or access specifiers. There are some more access specifiers like public, private, default, protected.
These are used to provide access for other files to access this code. For example: "public class" can be accessed from all the other files.

3. Consider the below program to print "Hello World!"(**output something**),
```java
public class Main{
	public static void main(String[] args){
		System.out.println("Hello World!");
	}
}
```
- In this above code, this line "public static void main(String[] args)" indicates the main function. No program can start running without main function in it. All the program will start to run from main function. Functions inside classes are called "methods". So, "public static void main(String[] args)" is also a method of class main. 
- The keyword "static" is used here to run the main functions without creating any object of class Main.
- The keyword "void" is the return type of main function(void means no return values).
- "Strings[] args" is called arguments. Arguments are used to pass values of one function to other function.

4. "System.out.println("Hello World!")", in this line, System is a class name, out is a variable inside that class and println is a function which prints.

5. Whenever we compile our code using "javac Main.java", a ".class" file will be created in the same folder which contains byte code. If you want that ".class" file in the previous folder, then use "javac -d .. Main.java". And to run that ".class" file, we use the command "java Main".

6. There is a concept called packages in java. They are like a folder in which your java program file lies. Packages can be simply defined as a set of classes or interfaces grouped together. We can also say like, these classes inside these package1 can be accessed from package2 only.

7. Consider this program to get input from the user(**Input something**),
```java
import java.utils.Scanner;

public class Main{
	public static void main(Sting[] args){
		Scanner input = new Scanner(System.in);
		System.out.println(input.nextInt()); //Integer input
		System.out.println(input.next()); //one word string
		System.out.println(input.nextLine()); //one line of sentence
		
	}
}
```

# Primitives and non-primitives

Any datatype that cannot be divided further is called primitive datatypes. And any datatype that can be divided further is called non-primitive datatypes.
**Primitive data types** - includes byte , short , int , long , float , double , boolean and char.
**Non-primitive data types** - such as String , Arrays and Classes.

# Variable declaration

consider the following code for declaring variables for different datatypes,
```java
public class Main{
	public static void main(String[] args){
		int rollno = 181; //can store only 4 bytes
		char letter = 'J';
		float marks = 99.9f; //can store only 4 bytes
		double largeDecimalNumbers = 234587.43455; //can store only 8 bytes
		long largeInteger = 122334234344866563L;//can store only 8 bytes
		boolean check = true;

		//we can also create wrapper classes like
		Integer rno = 10;//to get more functionalities to primitives
	}
}
```

- All the decimal values are "double" by default. If we want to store them in float, then we must use "f" at the last.
- Normal numbers without decimals are "int" by default. If we want to store them in long, then we must use "L" at the last.
