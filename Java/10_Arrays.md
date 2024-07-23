## Why arrays?

- **Efficient Access**: Direct element access with index (O(1) time complexity).
- **Memory Management**: Contiguous memory allocation enhances cache performance and reduces overhead.
- **Ease of Use**: Simple to declare and well-supported in most languages.
- **Fixed Size**: Predictable memory usage when element count is known.
- **Iteration**: Easy to loop through elements.
- **Compatibility**: Works well with other data structures and algorithms.
- **Multi-Dimensional Data**: Supports complex structures like matrices.
- **Mathematical Operations**: Essential for efficient numerical and scientific computations.

#### Syntax:

```java
int nums[] = {1, 2, 3};
//or
int nums[] = new int[4];
```

### Memory allocation of array

```java
public class Main{
	public static void main(String[] args){
		int nums[9] = {40, 55, 63, 17, 22, 68, 89, 97, 89};
	}
}
```
![[memoryForArray.png]]

- Array has contiguous allocation of memory.

### Printing array elements
each element in the array will have an index for it. Index value starts from 0 and end with n-1.

```java
public class Main{
	public static void main(String[] args){
		int arr[] = {3, 5, 7, 9};
		arr[2] = 4;    //can change the value of array elements
		for(int i = 0; i < 4; i++){
			System.out.println(arr[i]);
		}
	}
}
```

### Dynamic array

```java
public class Main{
	public static void main(String[] args){
		int arr[] = new int[4];   //by default, all the values are 0.
		arr[0] = 2;
		arr[1] = 3;
		arr[2] = 5;
		arr[3] = 7;
		for(int i = 0; i < 4; i++){
			System.out.println(arr[i]);
		}
	}
}
```

## Multi-dimensional array

We can call a multi-dimensional array as array of array.
Consider this 2D array...
![[2DArray.png]]
#### Syntax:

```java
int nums[][] = new int[3][4]

//or

int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7, 2}, {1, 2, 3, 4}, {5, 6, 7, 2} };
```

Here, 3 is the number of rows and 4 is the number of columns.
![[2DArrayIndex.png]]


#### Example:

```java
public class Main{
	public static void main(String[] srgs){
		int num[][] = new int[3][4];
		//assigning some random values
		for(int i = 0; i < 3; i++){
			for(int j = 0; j < 4; j++){
				num[i][j] = (int)(Math.random() * 10);
			}
		}


		for(int i = 0; i < 3; i++){
			for(int j = 0; j < 4; j++){
				System.out.print(num[i][j] + " ");
			}
			System.out.println();
		}
	}
}
```

Using enhanced loop,
```java
public class Main{
	public static void main(String[] srgs){
		int num[][] = new int[3][4];
		//assigning some random values
		for(int i = 0; i < 3; i++){
			for(int j = 0; j < 4; j++){
				num[i][j] = (int)(Math.random() * 10);
			}
		}


		for(int n[]: num){      //selects a row
			for(int m: n){            //selects a column in that selected row
				System.out.print(m + " ");
			}
			System.out.println();
		}
	}
}
```


## Jagged Arrays

When we have different number of columns in each rows, then we call it as an jagged array in java.

#### Example:

```java
public class Main{
	public static void main(String[] srgs){
		int nums[][] = new int[3][];    //jagged
		nums[0] = new int[3];
		nums[1] = new int[4];
		nums[2] = new int[2];

		for(int i = 0; i < nums.length; i++){
			for(int j = 0; j < nums[i].length; j++){
				nums[i][j] = (int)(Math.random() * 10);
			}
		}

		for(int n[]: nums){
			for(int m: n){
				System.out.print(m + " ");
			}
			System.out.println();
		}
	}
}
```

Consider this 3D array, 
It is like, array of array of array.

#### Example:

```java
public class Main{
	public static void main(String[] srgs){
		int nums[][][] = new int[3][4][5];

		for(int i = 0; i < nums.length; i++){
			for(int j = 0; j < nums[i].length; j++){
				for(int k = 0; k < nums[i][j].length; k++){
						nums[i][j][k] = (int)(Math.random() * 10);
				}
			}
		}

		for(int n[][]: nums){
			for(int m[]: n){
				for(int o: m){
					System.out.print(o + " ");
				}
				System.out.println();
			}
			System.out.println();
		}
	}
}
```

## Drawbacks of array

- Array is an object in java when we use a keyword called 'new' to store it in heap memory.
- Array size is static. int arr[] = new int[4];----> this can only have 4 values and not more than that. If we have to store more values than that, then we have create a new array with increased size and then copy the elements to that array.
- Only if you know the size of an array, then only you can go with it.

## Array of objects 

\[**Exception** - Run time errors are called Exceptions\]

- To find length of an array, we can use 'arr.length'.


#### Example:

```java
class Student{
	String name;
	int rollnum;
	int marks;
}
public class Main{
	public static void main(String[] args){
		Student s1 = new Student();
		s1.name = "ravi";
		s1.rollnum = 10;
		s1.marks = 100;

		Student s2 = new Student();
		s2.name = "ram";
		s2.rollnum = 7;
		s2.marks = 99;

		Student s3 = new Student();
		s3.name = "rani";
		s3.rollnum = 4;
		s3.marks = 98;


		Student student[] = new Student[3];
		student[0] = s1;
		student[1] = s2;
		student[2] = s3;

		for(int i = 0; i < student.length; i++){
			System.out.println(student[i].name +": "+ student[i].marks +": "+ student[i].rollnum);
		}
	}
}
```


## Enhanced for loop

#### Example
```java
for(int n: nums){
	System.out.println(n);
}
```

Using this syntax for the above array of objects example,
```java
for(Student stud : student){
	System.out.println(stud.name+":"+stud.rollnum+":"+stud.marks);
}
```
