- Basically string is an object in java and it is an non-primitive datatype with capital letter at first(String). 
- Strings are enclosed within double quotes.
- we can have the string as an array of characters.
- Strings can only work with addition operator(used for concatenation). No other operators can be implemented in strings.
#### Example:
Consider the example of printing a name.

```java
public class Main{
	public static void main(String[] args){
		String name = new String("Jothshana");
		System.out.println("Hello " + name);
	}
}
```

And also we have several methods for name here...
```java
public class Main{
	public static void main(String[] args){
		String name = new String("Jothshana");
		System.out.println("Hello " + name);          //Hello Jothshana
		System.out.println(name.charAt(1));           //o
		System.out.println(name.concat(" S M"));      //Jothshana S M
	}
}
```

In Java string are an important concept, so to make this more easier, we can also create a string like, 
```java
public class Main{
	public static void main(String[] args){
		String name = new String("Jothshana");
		// or
		String name = "Jothshana";
		//Both are same. A new object will be created for this without using the keyword 'new'.
	}
}
```

#### Example:
What will happen if you change the value of a string?
```java
public class Main{
	public static void main(String[] args){
		String name = "joe";
		name = name + " Jothshana"         //a new object will be created in the heap memory.
		System.out.println(name);            //joe Jothshana

		String s1 = "JO";
		String s2 = "JO";          // Both s1 and s2 are pointing to the same memory address in the heap memory. That means, they are pointing to a single object.
	}
}
```

This is because, we have a thing called string constant pool inside the heap memory. It does not allows duplicate objects inside it. Thus, when we have same data for 2 different string variables, then both variable will point to a single memory address in the string constant pool. And when we reassign a value to any variable, it creates another object inside the string constant pool and also the old data of that variable will get hit by garbage collection.

We have two different types of strings, one is mutable(can change) and another one is immutable(cannot change).

## String Buffer and String Builder

If we want to create mutable string, we will use either String Buffer or String Builder.

#### Example:
```java
public class Main{
	public static void main(String[] args){
		StringBuffer sb = new StringBuffer("jothshana");
		System.out.println(sb.capacity());
		System.out.println(sb.length());
		sb.apppend(" S M");
		sb.deleteCharAt(0);
		System.out.println(sb);

		String str = sb;
		String str1 = sb.toString();


		//add also we have several methods in this...eg: append, insert, delete, sub-string and more...
	}
}
```

There is only one difference between StringBuffer and StringBuilder that is StringBuffer is thread-safe and synchronized whereas  StringBuilder is not. That's why StringBuilder is faster than StringBuffer.


