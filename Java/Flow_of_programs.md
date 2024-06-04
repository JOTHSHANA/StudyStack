
# Flowcharts

Flowcharts are visual representations of the steps or processes involved in a program or algorithm. They use various symbols to denote different types of actions or steps, and arrows to show the flow and sequence of these steps. Flowcharts are useful for planning and documenting the logic of a program before coding it, making it easier to understand, communicate, and troubleshoot.

### Symbols:

![flowchart_symbols](https://www.smartdraw.com/flowchart/img/basic-symbols-table.jpg)


#### Example:

###### Odd/Even

<img src="https://technologystrive.com/static/0d252430f6c54dbdec7ea1dd9f0ba281/59000/FlowChart_EvenOdd.png" height="400" />


###### Prime/not

![[Pasted image 20240604185313.png]]



# Pseudo code

Pseudo code is a plain-language description of a program's logic and structure, using simple variables, control structures, and functions without specific syntax. It aims to clearly outline the steps and flow of an algorithm, making it easy to understand and translate into actual code, thus bridging the gap between concept and implementation.

###### Odd/Even
```PseudoCode
START 
	// Input a number 
	INPUT number 
	// Check if the number is even
	IF number MOD 2 == 0 THEN
		PRINT "The number is even"
	ELSE
		PRINT "The number is odd" 
	END IF
END
```

###### Prime/Not
```PseudoCode
START
	// Input a number
	INPUT number
  
	// Assume the number is prime
	SET isPrime TO true

	// Check for factors from 2 to the square root of the number
	IF number <= 1 THEN
	    SET isPrime TO false
	ELSE
	    FOR i FROM 2 TO sqrt(number) DO
			IF number MOD i == 0 THEN
				SET isPrime TO false
				BREAK
			END IF
	    END FOR
	END IF

	// Output the result
	IF isPrime THEN
	    PRINT "The number is prime"
	ELSE
	    PRINT "The number is not prime"
	END IF
END
```

