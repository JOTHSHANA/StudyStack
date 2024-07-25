# Static variables

#### Example:
```java
class Mobiles{
	String brand;
	int price;
	static String name;  //to have same name for all the objects

	public void show(){
		System.out.println(brand + ":" + price + ":" + name);
	}
}
public class Main{
	public static void main(String[] args){
		Mobiles obj1 = new Mobiles();
		obj1.brand = "Apple";
		obj1.price = 2000;
		Mobiles.name = "smartPhone";

		Mobiles obj2 = new Mobiles();   // static variables are called using class name....not with objects name.
		obj2.brand = "Android";
		obj2.price = 1000;
		Mobiles.name = "smartPhone";

		Mobiles.name = "Phone"; //This will affect all the object's name.
		// now, all the objects will have same value for name.

		obj1.show();
		obj2.show();
	}
}
```

# Static methods

- non-static variables cannot be used inside static methods. 

```java
class Mobiles{
	String brand;
	int price;
	static String name;  //to have same name for all the objects

	public void show(){
		System.out.println(brand + ":" + price + ":" + name);
	}

	public static void show1(Mobile obj){
		System.out.println(obj.brand + ":" + obj.price + ":" + obj.name);
	}
}
public class Main{
	public static void main(String[] args){
		Mobiles obj1 = new Mobiles();
		obj1.brand = "Apple";
		obj1.price = 2000;
		Mobiles.name = "smartPhone";

		Mobiles obj2 = new Mobiles();   // static variables are called using class name....not with objects name.
		obj2.brand = "Android";
		obj2.price = 1000;
		Mobiles.name = "smartPhone";

		Mobiles.name = "Phone"; //This will affect all the object's name.
		// now, all the objects will have same value for name.

		obj1.show();
		obj2.show();

		Mobiles.show1();  //it is not possible like this.
		Mobiles.show1(obj1);
	}
}
```

This is the reason why main is a static method.

# Static block

In Java, a static block, also known as a static initialization block, is used for static initialization of a class. It is a block of code that gets executed when the class is loaded into the memory by the Java Virtual Machine (JVM). Static blocks are typically used to initialize static variables or to perform some logic that needs to be executed once when the class is first loaded.

#### Example
```java
public class Example {
    static int staticVariable;

    // Static block
    static {
        staticVariable = 10;
        System.out.println("Static block executed. staticVariable = " + staticVariable);
    }

    public static void main(String[] args) {
        System.out.println("Main method executed.");
        System.out.println("staticVariable = " + staticVariable);
    }
//Output:
//Static block executed. staticVariable = 10
//Main method executed. 
//staticVariable = 10
}
```

In this example,
- The static block initializes the `staticVariable` to 10.
- The static block runs before the main method when the class is loaded.
- You will see the output from the static block first, followed by the output from the main method.

#### **Key points about static blocks:**

- Static blocks are executed in the order they appear in the class.
- They are executed only once, when the class is first loaded.
- Multiple static blocks can be declared in a class.
- They are useful for initializing static variables or performing static initialization logic.