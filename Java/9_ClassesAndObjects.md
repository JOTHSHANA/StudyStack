## Classes
A class is a blueprint or prototype from which objects are created. It can contain fields (variables) and methods (functions) to define the properties and behaviors of the objects.
#### Syntax:
```java
public class ClassName {
    // fields
    int field1;
    String field2;

    // methods
    void method1() {
        // method body
    }

    int method2() {
        // method body
        return 0;
    }
}
```
## Objects
In the context of OOP, everything in the world can be considered an object. All objects have certain properties and behaviors. In Java, objects are instances of classes. A class serves as a blueprint for creating objects. When a class is defined, no memory is allocated until an object of that class is created. Objects have state (defined by the fields) and behavior (defined by the methods). Here, the class name will act as a variable name.

#### Example:

```java
// Define a class named Calculator
class Calculator {
	int a; //can also have variables inside a class
    // Method to add two integers
    public int add(int n1, int n2) {
        System.out.println("Hii");
        int res = n1 + n2;
        return res;
    }
}

public class Main {
    public static void main(String[] args) {
        int num1 = 5;
        int num2 = 6;
        // Create an object of the Calculator class
        Calculator calc = new Calculator(); //calc --> reference variable
        // Call the add method of Calculator and store the result
        int output = calc.add(num1, num2);
        System.out.println(output);
    }
}
```


## Role of JDK, JRE and JVM in OOPS

JVM generally runs the byte code. Assume that we have a file with byte code inside JVM, Obviously the file may depend upon some other files to run. Here, JRE comes into picture, it provides all the dependency files and library files to JVM to successfully run a program.

![[Architecture.png]]


## Methods

Methods are nothing but the functions inside classes. main is also a method in java as it is present in a class. main is a method from where the program starts its execution. A class can have multiple methods inside it.

#### Example:

```java
class Computer{
	public void playMusic(){
		System.out.println("Playing Music!!");
	}

	public String getAPen(int cost){
		if(cost >= 10){
			return "Pen";
		}
		return "No Pen";
	}
}
public class Main{
	public static void main(String[] args){
		Computer comp = new Computer();
		comp.playMusic();
		String res = comp.getAPen(15);
		System.out.println(res);
	}
}
/* Output:
	Playing Music!!
	Pen
*/
```

**NOTE:**
Whenever the program encounters a "return" keyword, it exits the correct method(function will end). 

## Method Overloading
Method overloading in Java is a feature that allows a class to have more than one method with the same name, but with different parameter lists. These different parameter lists can vary by the number of parameters, the type of parameters, or both. Method overloading is an example of compile-time polymorphism, where the method to be called is determined at compile time.

```java
class MathOperations {
    // Method to add two integers
    public int add(int a, int b) {
        return a + b;
    }
    // Overloaded method to add three integers
    public int add(int a, int b, int c) {
        return a + b + c;
    }
    // Overloaded method to add two double values
    public double add(double a, double b) {
        return a + b;
    }
    // Overloaded method to add an integer and a double
    public double add(int a, double b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        MathOperations mathOps = new MathOperations();
        System.out.println(mathOps.add(5, 3)); // Calls add(int, int)
        System.out.println(mathOps.add(5, 3, 2)); // Calls add(int, int, int)
        System.out.println(mathOps.add(5.5, 3.3)); // Calls add(double, double)
        System.out.println(mathOps.add(5, 3.3)); // Calls add(int, double)
    }
}

```

## Stack and Heap in java

The memory inside JVM can be divided into two parts. They are stack and heap. Stack follow last in first out. There will be separate stack for each method in java.

Consider the following example to get clear with how memory works.
#### Example

```java
class Calculator {
	int a;

    public int add(int n1, int n2) {
        System.out.println("Hii");
        return n1 + n2;
    }
}

public class Main {
    public static void main(String[] args) {
        int data = 10;
        Calculator obj = new Calculator(); 
        Calculator obj1 = new Calculator(); 
        int r1 = calc.add(3,4);
        System.out.println(r1);
    }
}
```

In this above program we have 2 stack. one is for main method and another one is for add method. Now the object which is created in the main method will get stored inside the heap memory. Every time when we call the object, it is called from heap memory. The address of the object in heap memory is stored in the stack of main method(because obj is a reference variable). Observe the below figure,

![[stackAndHeap.png]]
In fact if we change the value obj.num = 15, then one obj will have the num value as 15. obj1 will have the same value 5.

