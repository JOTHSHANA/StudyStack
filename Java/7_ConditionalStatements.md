
Conditional statements in Java are used to make decisions based on certain conditions. The most common conditional statements in Java are the If-Else statement, the Switch statement, and the Ternary Operator. These statements allow the program to execute different blocks of code based on specific conditions.

## If / If-else statements

**NOTE**:
- if block is also called as true block. whenever the given condition id true, if block will get executed and if false, else block will get executed.
- If , if block has only one statement to execute then the curly brackets can be avoided if needed.
#### Example 1:

```java
public class Main{
	public static void main(String[] args){
		int x = 20;
		if(x >= 18){
			System.out.println("Hello");
		} 
		// output: Hello
		// if value of x is lesser then 18 then noting will get printed.
	}
}
```

#### Example 2:

```java
public class Main{
	public static void main(String[] args){
		int x = 20;
		if(x >= 18){
			System.out.println("Hello");
		}
		else{
			System.out.println("Bye");
		}
		// Output: Hello
		// if the value of x is lesser than 18, then the output will be : Bye
	}
}
```

#### Example 3:

```java
public class Main{
	public static void main(String[] args){
		int a = 2;
		int b = 4;
		
		if(a <= 5 && b <= 10)
			System.out.println("Satisfied");
		else
			System.out.println("Not satisfied");

		// output : Satisfied
		
		if(a >= 5 || b <= 10)
			System.out.println("Satisfied");
		else
			System.out.println("Not satisfied");
		//output : Not satisfied
	}
}
```

#### Example 4 (Finding maximum of two numbers):

```java
public class Main{
	public static void main(String[] args){
		int x = 10;
		int y = 20;
		if(x > y)
			System.out.println("x is larger");
		else
			System.out.println("y is larger");
		// output: y is larger
	}
}
```

#### Example 5 (Finding maximum of three numbers):

```java
public class Main{
	public static void main(String[] args){
		int x = 10;
		int y = 20;
		int z = 30;

		if(x > y && x > z){
			System.out.println("x is larger");
		}
		else{
			if(y > z)
				System.out.println("y is larger");
			else
				System.out.println("z is larger");
		}
	}
}
```

## Else-if

If we have multiple conditions to check, then we can have 'else if' block in our code.
```java
public class Main{
	public static void main(String[] args){
		int x = 10;
		int y = 20;
		int z = 30;

		if(x > y && x > z)
			System.out.println("x is larger");
		else if(y > z)
			System.out.println("y is larger");
		else
			System.out.println("z is larger");
		//output: z is larger
	}
}
```

\
## Ternary operator

- This is a shortcut for using if-else statements.
- If there is only one statement to be executed inside the if and else block then only we can use ternary operator. If the blocks have multiple statements to execute, then ternary operator cannot be used.
#### Example 1:

```java
public class Main{
	public static void main(String[] args){
		int x = 10;
		int y = 20;
		String res = x < y? "Yes" : "No";
		System.out.println(res);
	}
}
```

#### Example 2 (Odd/Even):

```java
public class Main{
	public static void main(String[] args){
		int x = 10;
		String res = x%2 == 0? "Even":"Odd";
		System.out.println(res);
	}
}
```

#### Example 2 (Maximum of three numbers):

```java
public class Main{
	public static void main(String[] args){
		int x = 10;
		int y = 20;
		int z = 30;

		int res = x>y && x>z? x: y>z? y: z;

		System.out.println(res);

		//output: 30
	}
}
```



## Switch statements

This can switch between multiple cases and then execute the correct block of code.

#### Example 1:

using else-if, 

```java
public class Main{
	public static void main(String[] args){
		int n = 2;

		if(n == 1)
			System.out.println("Sunday");
		if(n == 2)
			System.out.println("Monday");
		if(n == 3)
			System.out.println("Tuesday");
		if(n == 4)
			System.out.println("Wednesday");
		if(n == 5)
			System.out.println("Thursday");
		if(n == 6)
			System.out.println("Friday");
		if(n == 7)
			System.out.println("Saturday");
	}
}
```

but, instead of this this we can go with switch statements

using switch, 

```java
public class Main{
	public static void main(String[] args){
		int n = 5;

		switch(n){
			case 1:
				System.out.println("Sunday");
				break;
			case 2:
				System.out.println("Monday");
				break;
			case 3:
				System.out.println("Tuesday");
				break;
			case 4:
				System.out.println("Wednesday");
				break;
			case 5:
				System.out.println("Thursday");
				break;
			case 6:
				System.out.println("Friday");
				break;
			case 7:
				System.out.println("Saturday");
				break;
			default:
				System.out.println("Enter a valid number");
		}
	}
}
```

Switch statements can also support Strings,
#### Example 2:

```java
public class Main{
	public static void main(String[] args){
		String day = "Sunday";

		switch(day){
			case "Saturday", "Sunday":
				System.out.println("8am");
				break;
			case "Monday":
				System.out.println("6am");
				break;
			case "Tuesday":
				System.out.println("6am");
				break;
		}
	}
}
```

Instead of using break statements in each case, there is one more way to write this. Consider the following(This code will function only the latest version of java compiler. Use 'OneCompiler' online to test this code).

```java
public class Main{
	public static void main(String[] args){
		String day = "Sunday";

		switch(day){
			case "Saturday", "Sunday" -> System.out.println("8am");
			case "Monday", "Friday" -> System.out.println("6am");
			case "Tuesday", "Wednesday", "Thursday" -> System.out.println("7am");
			default -> System.out.println("Invalid day");
		}
	}
}
```

instead of printing, we can also assign it to a variable. like, 
```java
public class Main{
	public static void main(String[] args){
		String day = "Sunday";
		String res = "";
		switch(day){
			case "Saturday", "Sunday" -> res = "8am";
			case "Monday", "Friday" -> res = "6am";
			case "Tuesday", "Wednesday", "Thursday" -> res = "7am";
			default -> System.out.println("Invalid day");
		}
		System.out.println(res);
	}
}

```

it can be also written as, 
```java
public class Main{
	public static void main(String[] args){
		String day = "Sunday";
		String res = "";
		res = switch(day){
			case "Saturday", "Sunday" ->"8am";
			case "Monday", "Friday" ->"6am";
			case "Tuesday", "Wednesday", "Thursday" ->"7am";
	    default -> "invalid";
		};
		System.out.println(res);
	}
}
```

instead of arrow (->), you can use a colon with the keyword yield( : yield).
consider the following, 
```java
public class Main{
	public static void main(String[] args){
		String day = "Sunday";
		String res = "";
		res = switch(day){
			case "Saturday", "Sunday" : yield "8am";
			case "Monday", "Friday" : yield "6am";
			case "Tuesday", "Wednesday", "Thursday" : yield "7am";
	    default : yield "invalid";
		};
		System.out.println(res);
	}
}
```