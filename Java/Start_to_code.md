
## JShell

JShell is an interactive tool introduced in Java 9 that allows for quick testing and exploration of Java code. It provides immediate feedback on code snippets, making it ideal for learning and rapid prototyping. You can run Java statements, expressions, and declarations directly without writing a full program. To start JShell, simply run the `jshell` command in your terminal. This tool is beneficial for exploratory programming and can integrate with other development environments.

### sample:

![[jshell.png]]


## Behind the scenes
### Key Java Components

**JVM** - Java Virtual Machine
**JRE** - Java Runtime Environment
**JDK** - Java Development Kit
JDK will have JRE and JVM inside it.

Java is called as "**WORA**". This means that **Write Once and Run Anywhere**.

The operating system runs on top of the hardware. The JRE runs on top of the operating system, and the JVM is present inside the JRE, providing the needed libraries to the JVM. The JVM is platform-dependent, while Java is platform-independent. Any Java program we write is executed by the JVM. The problem is that the JVM cannot understand Java code directly. Instead, Java code must be converted into bytecode (.class file), which is then given to the JVM to run. The JVM executes the file that contains the main function. The Java code is converted to bytecode by the compiler (javac).


![[behindScenes.png]]

### Commands
- Java to byte code(compiling) - **javac file.java**
- Run program - **java classNameInsideThatFile**



