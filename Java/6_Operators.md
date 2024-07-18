
## Arithmetic operators

Arithmetic operators are used to perform operations among numbers like addition, subtraction, multiplication, division and modulus.

![[arithmeticOperators.png]]


#### Example:

```java
public class Main{
	public static void main(String[] args){
		int num1 = 5;
		int num2 = 3;

		int res1 = num1+num2; // Output: 8
		int res2 = num1-num2; // Output: 2
		int res3 = num1*num2; // Output: 15
		int res4 = num1/num2; // Output: 1
		int res5 = num1%num2; // Output: 2
		
	}
}
```


### Shortcuts operators

![[shorthandOperators.png]]

#### Example:

```java
public class Main{
	public static void main(String[] args){
		int num = 10;

		num += 2;   // Output: 12
		num -= 2;   // Output: 8
		num *= 2;   // Output: 20
		num /= 2;   // Output: 5
		num %= 3;   // Output: 1
	}
}
```


### Increment and Decrement

To add or subtract a number by 1, we can use these two operators.

```java
public class Main{
	public static void main(String[] args){
		int num = 2;
		//assume the value of num is 2 in all the lines and then calculate the result
		num++; // 3  this is equal of doing num = num+1;
		num--; // 1
		++num; // 3
		--num; // 1

		int num2 = ++num; // 3 (increament and assign)
		int num1 = num++; // 2 (assign and increament)
		
	}
}

```


- increment or decrement operator at the front of the variable like '++a' or '--a' is called pre-increment or pre-decrement.
-  increment or decrement operator at the back of the variable like 'a++' or 'a--' is called post-increment or pre-decrement.


## Relational Operators

![[relationalOperators.png]]


Relational operators can compare two values and provide the output in Boolean (true or false).

```java

public class Main{
	public static void main(String[] args){
		int a = 5;
		int b = 6;

		boolean res1 = a > b;   //false
		boolean res2 = a < b;   //true
		boolean res3 = a <= b;  //true
		boolean res4 = a >= b;  //false
		boolean res8 = a != b;  //true

		int x = 5;
		int y = 5;

		boolean res5 = x >= y;   //true
		boolean res6 = x <= y;   //true
		boolean res7 = x == y;   //true
		boolean res9 = x != y;  //false

		double n1 = 9.4;
		double n2 = 4.5;

		boolean res10 = n1 >= n2;  //true
	}
}
```



## Logical operators

Two relational operators which can result in true or false. Combining two relational statement into one logical statement can result in either true or false.

There are three main logical operators. They are AND (&), OR(|), NOT(!).

![[gates.png]]

In programming we can use short circuit operators like, `&&` for AND, `||` for OR , `!` for NOT.

```java

public class Main{
	public static void main(String[] args){
		int a = 10;
		int b = 13;
		int x = 2;
		int y = 5;

		boolean res1 = a < b && x < y;  // true
		boolean res2 = a > b && x < y;  // false
		boolean res3 = a < b || x < y;  //true
		boolean res4 = a > b || x < y;  //true

		System.out.println(!res4);
	}
}
```

