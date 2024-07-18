## Loops

Whenever a piece of code is repeated continuously, in order to avoid code continuous repetition, we go to a concept called loops. There are many types for loops in java. They are,
- while loop
- do while loop
- for loop
## While loop

 While loop will continuously run a block of statements again and again until it reaches certain condition.
```java
 //initialization
 while(condition){
	 //statements
	 //increment/decrement
 }
```

#### Example 1:
**Print "Hi" for 5 times using while loop**
like Hi1 Hi2 ...Hi5, then bye and i value at last

```java
public class Main{
	public static void main(String[] args){
		int i = 1;
		while(i <= 5){
			System.out.print("Hi"+i+" ");
			i++;
		}
		System.out.print("Bye"+i);
	}
}
//Output: Hi1 Hi2 Hi3 Hi4 Hi5 Bye6
```

#### Example 2:
**Print one 'hi' and three 'hello' in a line for 5 times with their iteration number**

```java
public class Main{
	public static void main(String[] args){
		int i = 1;
		while(i<= 5){
			System.out.print("Hi" + i);
			int j = 1;
			while(j <= 3){
				System.out.print(" Hello" + j);
				j++;
			}
			System.oy.println("");
			i++;
		}
	}
}
//Output:
/*Hi1 Hello1 Hello2 Hello3
Hi2 Hello1 Hello2 Hello3
Hi3 Hello1 Hello2 Hello3
Hi4 Hello1 Hello2 Hello3
Hi5 Hello1 Hello2 Hello3*/
```


## Do-While loop
Even if the condition is false, the loop will get executed at least once.
```java
//initialization
do{
	//statements
	//increment/decrement
}while(condition);
```
#### Example 1:

```java
public class Main{
	public static void main(String[] args){
		int i = 5;
		do{
			System.out.println("Hi"+ i);
			i++;
		}
		while(i <= 4);
	}
}
```

## For loop

```java
for(initialization;condition;increment/decrement){
	//statements
}
```

#### Example 1:
Print Hi1 Hi2...Hi5
```java
public class Main{
	public static void main(String[] args){
		for(int i = 1; i <= 5; i++){
			System.out.print("Hi" + i + " ");
		}
	}
}
//Output: Hi1 Hi2 Hi3 Hi4 Hi5
```

To reverse the above output, we can rewrite the code as, 

```java
public class Main{
	public static void main(String[] args){
		for(int i = 5; i >= 1; i--){
			System.out.print("Hi" + i + " ");
		}
	}
}
//Output: Hi5 Hi4 Hi3 Hi2 Hi1
```

- Remember a point that it is always a good practice to start the i value from 0 instead of 1. This is because, the index value will always start from 0 and ends with n-1. If you follow this, you can easily solve array problems without any confusion.

Consider this program for day 1 to day 3 with working hours from 9 to 18. Spliting working hours into one-one hour for scheduling.
```java
public class Main{
	public static void main(String[] args){
		for(int i = 1; i < 6; i++){
			System.out.println("Day:" + i);
			for(int j = 1; j < 10; j++){
				System.out.println((j+8) + "-" + (j+9));
			}
		}
	}
}

//Output:
/*Day:1
9-10
10-11
11-12
12-13
13-14
14-15
15-16
16-17
17-18
Day:2
9-10
10-11
11-12
12-13
13-14
14-15
15-16
16-17
17-18
Day:3
9-10
10-11
11-12
12-13
13-14
14-15
15-16
16-17
17-18
*/

```

#### Example 2:

Printing day 1 to day 5
```java
public class Main{
	public static void main(String[] args){
		int i = 1;
		for(;i<=5;){
			System.out.println("Day" + i);
			i++;
		}
	}
}

/*Output:
Day1
Day2
Day3
Day4
Day5
*/

```

- initialization, condition and increment/decrement can be missing from the for loop brackets but it is mandatory to have 2 semi-colons inside it.

#### Flow of for loop:
1. initialization
2. condition
3. inside block
4. increment/decrement
5. condition
6. inside block
7. step 4 to step 6 will get repeated until the condition fails.

### When to use which loop

- when you know the number of iterations, go with for loop.(printing 1 to 100).
- when you don't actually know the number of iterations, go with while loop(continuing the loop until a value becomes 0).
- when you think that, even if the condition is false, i have to execute the code once, then go with do-while loop(rare).

