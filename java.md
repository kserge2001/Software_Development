# Java Programming: A Comprehensive Guide

## Table of Contents
- [Introduction to Java](#introduction-to-java)
- [Setting Up Java Development Environment](#setting-up-java-development-environment)
- [Basic Syntax and Data Types](#basic-syntax-and-data-types)
- [Control Flow and Methods](#control-flow-and-methods)
- [Object-Oriented Programming](#object-oriented-programming)
- [Collections Framework](#collections-framework)
- [Exception Handling](#exception-handling)
- [File I/O and Streams](#file-io-and-streams)
- [Multithreading](#multithreading)
- [Java Standard Libraries](#java-standard-libraries)
- [Database Connectivity (JDBC)](#database-connectivity-jdbc)
- [GUI Programming](#gui-programming)
- [Testing with JUnit](#testing-with-junit)
- [Best Practices](#best-practices)
- [Additional Resources](#additional-resources)

## Introduction to Java

### What is Java?

Java is a high-level, class-based, object-oriented programming language that was developed by Sun Microsystems (which was later acquired by Oracle) in the mid-1990s. Java was designed to have as few implementation dependencies as possible, following the principle of "Write Once, Run Anywhere" (WORA), which means that compiled Java code can run on all platforms that support Java without the need for recompilation.

### History of Java

- 1991: A team led by James Gosling at Sun Microsystems began developing Java (initially called "Oak")
- 1995: Java 1.0 was officially released
- 1996: JDK 1.0 was released
- 1997: JDK 1.1 introduced many significant enhancements
- 1998: Java 2 (JDK 1.2) was released with major improvements
- 2004: Java 5 added generics, enums, annotations, etc.
- 2006: Sun made Java available as open-source software
- 2010: Oracle acquired Sun Microsystems and took control of Java
- 2014: Java 8 introduced lambda expressions and streams
- 2018: Oracle changed to a 6-month release schedule starting with Java 10
- 2023: Java 21 became the latest LTS (Long-Term Support) release

### Key Features of Java

- **Object-Oriented**: Everything in Java is an object that encapsulates data and behavior
- **Platform Independent**: Compiled Java bytecode can run on any device with a Java Virtual Machine (JVM)
- **Simple**: Java was designed to be easy to learn and use
- **Secure**: Java provides a secure execution environment
- **Multithreaded**: Java supports concurrent programming with built-in multithreading
- **Architecture-Neutral**: Java bytecode is architecture-neutral
- **Portable**: Java programs can run on any platform without modification
- **Robust**: Java includes strong memory management and exception handling
- **Dynamic**: Java is designed to adapt to evolving environments
- **High Performance**: Just-In-Time compiler ensures high performance

### Java Platforms

Java comes in different editions designed for different purposes:

- **Java SE (Standard Edition)**: Core platform for desktop and server applications
- **Java EE (Enterprise Edition)**: Built on top of SE, provides tools for large-scale, multi-tiered, scalable, reliable, and secure network applications
- **Java ME (Micro Edition)**: For developing applications for mobile devices
- **Java Card**: For applications running on smart cards and other small-memory devices

### Java in the Industry

Java is widely used in various domains:

- Enterprise Applications
- Web Applications and Services
- Mobile Applications (Android)
- Big Data Technologies (Hadoop, Spark)
- Financial Services
- Trading Applications
- Scientific Applications
- Embedded Systems

### Practice Exercise: Understanding Java Fundamentals

1. Research and list five popular applications built with Java
2. Compare Java with another programming language you're familiar with
3. Identify key reasons why companies choose Java for enterprise applications

## Setting Up Java Development Environment

### Installing Java

#### Installing JDK (Java Development Kit)

The JDK includes the Java Runtime Environment (JRE), an interpreter/loader (Java), a compiler (javac), an archiver (jar), and other tools for Java development.

##### Windows

1. Download the latest JDK from [Oracle's website](https://www.oracle.com/java/technologies/downloads/) or use OpenJDK
2. Run the installer and follow the instructions
3. Set up environment variables:
   - Set `JAVA_HOME` to your JDK installation directory
   - Add `%JAVA_HOME%\bin` to your Path variable

##### macOS

1. Using Homebrew (recommended):
   ```bash
   brew install openjdk
   ```

2. Or download the macOS installer from Oracle's website

##### Linux

```bash
# Ubuntu/Debian
sudo apt update
sudo apt install openjdk-17-jdk

# Fedora
sudo dnf install java-17-openjdk-devel

# Arch Linux
sudo pacman -S jdk-openjdk
```

#### Verifying Installation

Open a terminal or command prompt and run:

```bash
java -version
javac -version
```

You should see version information for both commands.

### Setting Up an IDE

#### Eclipse

1. Download Eclipse IDE for Java Developers from the [Eclipse website](https://www.eclipse.org/downloads/)
2. Extract the downloaded archive
3. Run the Eclipse executable
4. During first launch, specify a workspace directory
5. Configure Eclipse to use your installed JDK:
   - Go to Window > Preferences > Java > Installed JREs
   - Add your JDK installation directory

#### IntelliJ IDEA

1. Download IntelliJ IDEA from the [JetBrains website](https://www.jetbrains.com/idea/download/)
2. Run the installer and follow the instructions
3. Launch IntelliJ IDEA
4. Configure the JDK:
   - Go to File > Project Structure > Project
   - Select your JDK from the dropdown or add it if not listed

#### Visual Studio Code

1. Download and install VS Code from the [Visual Studio Code website](https://code.visualstudio.com/)
2. Open VS Code
3. Install the Java Extension Pack from the marketplace
4. Configure the JDK path in the settings

### Creating Your First Java Program

1. Open your IDE
2. Create a new Java project
3. Create a new Java class called `HelloWorld`
4. Add the following code:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

5. Save the file
6. Run the program using your IDE's run button

### Compiling and Running Java from the Command Line

```bash
# Navigate to the directory with your .java file
cd my_project

# Compile the Java file
javac HelloWorld.java

# Run the compiled program
java HelloWorld
```

### Understanding Java Project Structure

A typical Java project structure might look like:

```
my_project/
├── src/                    # Source code
│   ├── main/
│   │   ├── java/          # Java source files
│   │   │   └── com/
│   │   │       └── example/
│   │   │           └── MyApp.java
│   │   └── resources/     # Resource files (properties, XML, etc.)
│   └── test/              # Test code
│       └── java/
├── lib/                    # External libraries (JAR files)
├── bin/                    # Compiled class files
├── docs/                   # Documentation
└── README.md               # Project information
```

### Build Tools

#### Maven

Maven is a popular build automation tool for Java projects:

1. Install Maven
2. Create a new Maven project:
   ```bash
   mvn archetype:generate -DgroupId=com.example -DartifactId=my-app -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
   ```
3. Maven project structure:
   ```
   my-app/
   ├── pom.xml               # Project configuration file
   └── src/
       ├── main/
       │   └── java/
       │       └── com/
       │           └── example/
       │               └── App.java
       └── test/
           └── java/
               └── com/
                   └── example/
                       └── AppTest.java
   ```

#### Gradle

Gradle is another build automation tool that uses Groovy or Kotlin DSL:

1. Install Gradle
2. Create a new Gradle project:
   ```bash
   gradle init --type java-application
   ```

### Practice Exercise: Setting Up Your Java Environment

1. Install JDK on your machine and verify the installation
2. Set up an IDE of your choice (Eclipse, IntelliJ IDEA, or VS Code)
3. Create a simple Hello World program and run it
4. Create a simple Maven or Gradle project

## Basic Syntax and Data Types

### Java Program Structure

A basic Java program consists of:

```java
// Optional package declaration
package com.example;

// Optional imports
import java.util.Scanner;

// Class declaration
public class MyClass {
    // The main method - entry point of Java application
    public static void main(String[] args) {
        // Program statements
        System.out.println("Hello, World!");
    }
    
    // Additional methods
    public void anotherMethod() {
        // Method body
    }
}
```

### Comments in Java

Java supports three types of comments:

```java
// This is a single-line comment

/*
 * This is a
 * multi-line comment
 */

/**
 * This is a documentation comment (Javadoc)
 * @author Your Name
 * @version 1.0
 */
```

### Variables and Data Types

#### Primitive Data Types

Java has eight primitive data types:

```java
// Integer types
byte b = 100;                  // 8-bit signed, -128 to 127
short s = 10000;               // 16-bit signed, -32,768 to 32,767
int i = 100000;                // 32-bit signed, -2^31 to 2^31-1
long l = 10000000000L;         // 64-bit signed, -2^63 to 2^63-1

// Floating-point types
float f = 3.14f;               // 32-bit IEEE 754
double d = 3.14159265359;      // 64-bit IEEE 754

// Character type
char c = 'A';                  // 16-bit Unicode character

// Boolean type
boolean bool = true;           // true or false
```

#### Reference Data Types

Reference types store references to objects:

```java
// String (most commonly used reference type)
String greeting = "Hello, World!";

// Arrays
int[] numbers = {1, 2, 3, 4, 5};
String[] names = new String[3];

// Classes
Scanner scanner = new Scanner(System.in);

// Interface types
List<String> list = new ArrayList<>();
```

#### Type Conversion

```java
// Implicit conversion (widening)
int i = 100;
long l = i;    // int to long
float f = l;   // long to float
double d = f;  // float to double

// Explicit conversion (narrowing)
double d = 100.04;
long l = (long)d;   // double to long
int i = (int)l;     // long to int
```

### Variables and Constants

```java
// Variable declaration
int age;               // Declaration
age = 25;              // Assignment
int salary = 50000;    // Declaration and assignment

// Constants (using final keyword)
final double PI = 3.14159;
final String DATABASE_URL = "jdbc:mysql://localhost:3306/mydb";

// Variable naming conventions
int camelCaseVariable;    // Standard for variables
final int UPPER_CASE_CONSTANT = 100;  // Standard for constants
```

### Operators

#### Arithmetic Operators

```java
int a = 10, b = 3;
int sum = a + b;         // 13
int difference = a - b;  // 7
int product = a * b;     // 30
int quotient = a / b;    // 3
int remainder = a % b;   // 1

// Increment and decrement
int x = 5;
x++;                     // x is now 6 (postfix)
++x;                     // x is now 7 (prefix)
int y = 5;
int z = y++;             // z = 5, y = 6
int w = ++y;             // w = 7, y = 7
```

#### Comparison Operators

```java
int a = 10, b = 5;
boolean equal = (a == b);            // false
boolean notEqual = (a != b);         // true
boolean greater = (a > b);           // true
boolean less = (a < b);              // false
boolean greaterOrEqual = (a >= b);   // true
boolean lessOrEqual = (a <= b);      // false
```

#### Logical Operators

```java
boolean a = true, b = false;
boolean andResult = a && b;   // false
boolean orResult = a || b;    // true
boolean notResult = !a;       // false

// Short-circuit evaluation
boolean result = (getTrue() || getFalse());  // getFalse() is not called
```

#### Bitwise Operators

```java
int a = 5;  // 0101 in binary
int b = 3;  // 0011 in binary

int bitwiseAnd = a & b;       // 0001 (1)
int bitwiseOr = a | b;        // 0111 (7)
int bitwiseXor = a ^ b;       // 0110 (6)
int bitwiseComplement = ~a;   // 1...1010 (-6)
int leftShift = a << 1;       // 1010 (10)
int rightShift = a >> 1;      // 0010 (2)
int unsignedRightShift = a >>> 1; // 0010 (2)
```

#### Assignment Operators

```java
int a = 10;
a += 5;   // a = a + 5 (15)
a -= 3;   // a = a - 3 (12)
a *= 2;   // a = a * 2 (24)
a /= 4;   // a = a / 4 (6)
a %= 4;   // a = a % 4 (2)
a &= 3;   // a = a & 3 (2)
a |= 1;   // a = a | 1 (3)
a ^= 2;   // a = a ^ 2 (1)
a <<= 1;  // a = a << 1 (2)
a >>= 1;  // a = a >> 1 (1)
```

#### String Concatenation

```java
String firstName = "John";
String lastName = "Doe";
String fullName = firstName + " " + lastName;  // "John Doe"

// String + non-string
String message = "Age: " + 25;  // "Age: 25"
```

### Strings

Strings in Java are objects and offer various methods:

```java
// Creating strings
String s1 = "Hello";
String s2 = new String("Hello");

// String length
int length = s1.length();  // 5

// String methods
String upper = s1.toUpperCase();       // "HELLO"
String lower = s1.toLowerCase();       // "hello"
char character = s1.charAt(1);         // 'e'
int index = s1.indexOf('l');           // 2
boolean startsWith = s1.startsWith("He");  // true
boolean endsWith = s1.endsWith("lo

# Java Programming: A Comprehensive Guide

## Table of Contents
- [Introduction to Java](#introduction-to-java)
- [Setting Up the Development Environment](#setting-up-the-development-environment)
- [Basic Syntax and Concepts](#basic-syntax-and-concepts)
- [Object-Oriented Programming in Java](#object-oriented-programming-in-java)
- [Data Structures and Algorithms](#data-structures-and-algorithms)
- [File Handling and I/O](#file-handling-and-io)
- [Exception Handling](#exception-handling)
- [Collections Framework](#collections-framework)
- [Multithreading](#multithreading)
- [Java APIs and Libraries](#java-apis-and-libraries)
- [Database Connectivity (JDBC)](#database-connectivity-jdbc)
- [Unit Testing with JUnit](#unit-testing-with-junit)
- [Build Tools](#build-tools)
- [Real-World Project Examples](#real-world-project-examples)
- [Best Practices and Coding Standards](#best-practices-and-coding-standards)
- [Common Interview Questions](#common-interview-questions)
- [Resources for Further Learning](#resources-for-further-learning)

## Introduction to Java

### What is Java?
Java is a high-level, class-based, object-oriented programming language that was developed by Sun Microsystems (now owned by Oracle) in the mid-1990s. It's designed to have as few implementation dependencies as possible, enabling a "write once, run anywhere" (WORA) functionality.

### History of Java
- Created by James Gosling at Sun Microsystems in 1995
- Originally designed for interactive television
- Named "Oak" initially, then renamed to "Java"
- Sun Microsystems was acquired by Oracle Corporation in 2010

### Key Features of Java
- **Platform Independence**: Java code compiles to bytecode which runs on any device with a Java Virtual Machine (JVM)
- **Object-Oriented**: Based on the concept of objects containing data and methods
- **Simple**: Easier to learn compared to C++, removed complex features like pointers
- **Secure**: Runs in a virtual machine sandbox with robust memory management
- **Multithreaded**: Supports concurrent execution of multiple threads
- **Distributed**: Designed with network capabilities built-in
- **Dynamic**: Capable of dynamically linking new code modules
- **Architecture Neutral**: No implementation-dependent features
- **Portable**: Same code works across different platforms
- **High Performance**: Just-In-Time compiler enables high-speed execution
- **Robust**: Strong memory management, exception handling, type checking

### Java Editions
- **Java Standard Edition (Java SE)**: Core platform with libraries and APIs
- **Java Enterprise Edition (Java EE)**: For large-scale, distributed, enterprise applications
- **Java Micro Edition (Java ME)**: For mobile devices and embedded systems
- **JavaFX**: For creating rich internet applications with a modern UI

### Practice Exercise: Understanding Java's Place in Modern Development
1. Research and write a short essay (250 words) comparing Java to two other modern programming languages
2. List five real-world applications built with Java
3. Explain why Java remains relevant despite newer languages emerging

## Setting Up the Development Environment

### Installing the Java Development Kit (JDK)
1. Visit the [Oracle JDK download page](https://www.oracle.com/java/technologies/downloads/) or [OpenJDK](https://openjdk.java.net/)
2. Download the appropriate JDK for your operating system
3. Follow the installation instructions for your platform
4. Verify installation by opening a terminal and typing:
   ```
   java -version
   javac -version
   ```

### Setting Up Environment Variables
#### For Windows:
1. Right-click on "This PC" and select "Properties"
2. Click on "Advanced system settings"
3. Click on "Environment Variables"
4. Under System Variables, find and select "Path", then click "Edit"
5. Add the path to the JDK bin directory (e.g., `C:\Program Files\Java\jdk-17\bin`)
6. Create a new system variable called "JAVA_HOME" with the path to your JDK installation

#### For macOS/Linux:
1. Edit your profile file (~/.bash_profile, ~/.zshrc, etc.)
2. Add the following lines:
   ```
   export JAVA_HOME=/path/to/your/jdk
   export PATH=$JAVA_HOME/bin:$PATH
   ```
3. Apply changes with `source ~/.bash_profile` or restart your terminal

### Integrated Development Environments (IDEs)
#### IntelliJ IDEA
1. Download from [JetBrains website](https://www.jetbrains.com/idea/download/)
2. Community Edition is free and sufficient for most Java development
3. Installation is straightforward with a graphical installer

#### Eclipse
1. Download from [Eclipse website](https://www.eclipse.org/downloads/)
2. Choose "Eclipse IDE for Java Developers"
3. Extract the downloaded archive and run the Eclipse executable

#### VS Code with Java Extensions
1. Download [VS Code](https://code.visualstudio.com/)
2. Install the following extensions:
   - Extension Pack for Java
   - Java Debugger
   - Maven for Java
   - Java Test Runner

### Creating Your First Java Program
1. Open your IDE of choice
2. Create a new Java project
3. Create a new Java class file named "HelloWorld.java"
4. Enter the following code:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

5. Run the program to see "Hello, World!" printed in the console

### Practice Exercise: Environment Setup
1. Install the JDK and set up environment variables
2. Install an IDE of your choice
3. Create and run a "Hello, World!" program
4. Modify the program to accept your name as input and print a personalized greeting
5. Try compiling and running your program from the command line using `javac` and `java` commands

## Basic Syntax and Concepts

### Java Program Structure
- **Package Declaration**: Organizes classes (optional but recommended)
- **Import Statements**: Includes classes from other packages
- **Class Definition**: Container for code
- **Methods**: Define behavior
- **Main Method**: Entry point for execution

Example:
```java
// Package declaration
package com.example.basics;

// Import statement
import java.util.Scanner;

// Class definition
public class BasicSyntaxDemo {
    // Main method - program entry point
    public static void main(String[] args) {
        // Program code goes here
        System.out.println("Basic Java program structure demonstration");
    }
}
```

### Variables and Data Types
#### Primitive Data Types
- **byte**: 8-bit integer (-128 to 127)
- **short**: 16-bit integer (-32,768 to 32,767)
- **int**: 32-bit integer (-2^31 to 2^31-1)
- **long**: 64-bit integer (-2^63 to 2^63-1)
- **float**: 32-bit floating-point
- **double**: 64-bit floating-point
- **char**: 16-bit Unicode character
- **boolean**: true or false

#### Reference Data Types
- **String**: Sequence of characters
- **Arrays**: Collection of similar data types
- **Classes**: User-defined types
- **Interfaces**: Abstract types

#### Variable Declaration and Initialization
```java
// Variable declaration and initialization
int number = 10;
double pi = 3.14159;
char grade = 'A';
boolean isJavaFun = true;
String message = "Hello, Java!";
```

### Operators
#### Arithmetic Operators
```java
int a = 10, b = 5;
int sum = a + b;       // 15
int difference = a - b; // 5
int product = a * b;    // 50
int quotient = a / b;   // 2
int remainder = a % b;  // 0
```

#### Comparison Operators
```java
boolean isEqual = (a == b);     // false
boolean isNotEqual = (a != b);  // true
boolean isGreater = (a > b);    // true
boolean isLess = (a < b);       // false
boolean isGreaterOrEqual = (a >= b); // true
boolean isLessOrEqual = (a <= b);    // false
```

#### Logical Operators
```java
boolean condition1 = true, condition2 = false;
boolean andResult = condition1 && condition2; // false
boolean orResult = condition1 || condition2;  // true
boolean notResult = !condition1;              // false
```

#### Assignment Operators
```java
int x = 10;
x += 5;  // x = x + 5 (15)
x -= 3;  // x = x - 3 (12)
x *= 2;  // x = x * 2 (24)
x /= 4;  // x = x / 4 (6)
x %= 4;  // x = x % 4 (2)
```

### Control Flow Statements
#### Conditional Statements
```java
// if statement
int age = 20;
if (age >= 18) {
    System.out.println("You are an adult.");
}

// if-else statement
int time = 22;
if (time < 12) {
    System.out.println("Good morning.");
} else if (time < 18) {
    System.out.println("Good afternoon.");
} else {
    System.out.println("Good evening.");
}

// switch statement
int day = 3;
switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    // Additional cases
    default:
        System.out.println("Invalid day");
}
```

#### Looping Statements
```java
// for loop
for (int i = 0; i < 5; i++) {
    System.out.println("Iteration: " + i);
}

// while loop
int count = 0;
while (count < 5) {
    System.out.println("Count: " + count);
    count++;
}

// do-while loop
int num = 1;
do {
    System.out.println("Number: " + num);
    num++;
} while (num <= 5);

// for-each loop (enhanced for loop)
int[] numbers = {1, 2, 3, 4, 5};
for (int number : numbers) {
    System.out.println("Number: " + number);
}
```

#### Break and Continue
```java
// break example
for (int i = 1; i <= 10; i++) {
    if (i == 5) {
        break; // exits the loop when i equals 5
    }
    System.out.println(i);
}

// continue example
for (int i = 1; i <= 10; i++) {
    if (i % 2 == 0) {
        continue; // skips the rest of the loop for even numbers
    }
    System.out.println(i); // prints only odd numbers
}
```

### Methods
```java
// Method declaration
public static int add(int a, int b) {
    return a + b;
}

// Method call
int result = add(5, 3); // result = 8

// Method with void return type
public static void printMessage(String message) {
    System.out.println(message);
}

// Method overloading
public static double add(double a, double b) {
    return a + b;
}
```

### Arrays
```java
// Array declaration and initialization
int[] numbers = {1, 2, 3, 4, 5};

// Alternative initialization
int[] scores = new int[5]; // Creates an array of size 5 with default values (0)
scores[0] = 85;
scores[1] = 90;
scores[2] = 78;
scores[3] = 92;
scores[4] = 88;

// Accessing array elements
int firstNumber = numbers[0]; // 1
int thirdNumber = numbers[2]; // 3

// Array length
int arrayLength = numbers.length; // 5

// Multidimensional array
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
int value = matrix[1][2]; // 6
```

### Strings
```java
// String creation
String greeting = "Hello, Java!";
String name = new String("John");

// String concatenation
String fullName = "John" + " " + "Doe"; // "John Doe"

// String methods
int length = greeting.length(); // 12
char firstChar = greeting.charAt(0); // 'H'
String upperCase = greeting.toUpperCase(); // "HELLO, JAVA!"
String substring = greeting.substring(0, 5); // "Hello"
boolean containsJava = greeting.contains("Java"); // true
String[] parts = greeting.split(", "); // ["Hello", "Java!"]
String trimmed = "  Hello  ".trim(); // "Hello"
String replaced = greeting.replace("Java", "World"); // "Hello, World!"
```

### Practice Exercises: Basic Syntax and Concepts

#### Exercise 1: Variable Manipulation
Write a program that:
1. Declares variables of each primitive data type
2. Performs arithmetic operations with them
3. Displays the results

#### Exercise 2: Temperature Converter
Create a program that:
1. Accepts a temperature in Celsius
2. Converts it to Fahrenheit (F = C * 9/5 + 32)
3. Displays both temperatures

#### Exercise 3: Loop Practice
Write a program that:
1. Prints the first 10 Fibonacci numbers
2. Uses a loop of your choice

#### Exercise 4: Array Manipulation
Create a program that:
1. Creates an array of 10 integers
2. Fills it with random numbers between 1 and 100
3. Finds and displays the maximum, minimum, and average values

#### Exercise 5: String Processor
Write a program that:
1. Accepts a sentence as input
2. Counts the number of words
3. Counts the number of characters (excluding spaces)
4. Displays the sentence with the words in reverse order

## Object-Oriented Programming in Java

### Classes and Objects
#### Class Definition
```java
public class Person {
    // Fields (attributes)
    private String name;
    private int age;
    
    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    
    // Methods
    public void introduce() {
        System.out.println("Hi, I'm " + name + " and I'm " + age + " years old.");
    }
    
    // Getters and Setters
    public String getName() {
        return name;
    }
    
    public void setName(String name) {
        this.name = name;
    }
    
    public int getAge() {
        return age;
    }
    
    public void setAge(int age) {
        if (age >= 0) {
            this.age = age;
        }
    }
}
```

#### Creating and Using Objects
```java
// Creating objects
Person person1 = new Person("Alice", 25);
Person person2 = new Person("Bob", 30);

// Accessing object methods
person1.introduce(); // "Hi, I'm Alice and I'm 25 years old."
person2.introduce(); // "Hi, I'm Bob and I'm 30 years old."

// Using getters and setters
String name = person1.getName(); // "Alice"
person2.setAge(31);
System.out.println(person2.getAge()); // 31
```

### Encapsulation
Encapsulation is the mechanism of hiding the internal state of an object and requiring all interaction to be performed through an object's methods.

```java
public class BankAccount {
    // Private fields - encapsulated
    private String accountNumber;
    private String accountHolder;
    private double balance;
    
    // Constructor
    public BankAccount(String accountNumber, String accountHolder, double initialBalance) {
        this.accountNumber = accountNumber;
        this.accountHolder = accountHolder;
        if (initialBalance > 0) {
            this.balance = initialBalance;
        } else {
            this.balance = 0;
        }
    }
    
    // Public methods to interact with the private fields
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposited: $" + amount);
        } else {
            System.out.println("Invalid deposit amount");
        }
    }
    
    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawn: $" + amount);
        } else {
            System.out.println("Invalid withdrawal amount or insufficient funds");
        }
    }
    
    public double getBalance() {
        return balance;
    }
    
    public String getAccountInfo() {
        return "Account Number: " + accountNumber + ", Holder: " + accountHolder;
    }
    
    // No setter for accountNumber - can't be changed after creation
    // Limited access to sensitive data
}
```

### Inheritance

Inheritance is the mechanism by which a class can inherit attributes and methods from another class. It promotes code reusability and establishes a relationship between classes.

#### Base Class (Parent/Super Class)
```java
public class Animal {
    protected String name;
    protected int age;
    
    public Animal(String name, int age) {
        this.name = name;
        this.age = age;
    }
    
    public void eat() {
        System.out.println(name + " is eating.");
    }
    
    public void sleep() {
        System.out.println(name + " is sleeping.");
    }
    
    public String getName() {
        return name;
    }
    
    public int getAge() {
        return age;
    }
}
```

#### Derived Class (Child/Sub Class)
```java
public class Dog extends Animal {
    private String breed;
    
    public Dog(String name, int age, String breed) {
        super(name, age); // Call parent constructor
        this.breed = breed;
    }
    
    // Override parent method
    @Override
    public void eat() {
        System.out.println(name + " the " + breed + " is eating dog food.");
    }
    
    // New method specific to Dog
    public void bark() {
        System.out.println(name + " says: Woof Woof!");
    }
    
    public String getBreed() {
        return breed;
    }
}
```

#### Using Inheritance
```java
// Create an instance of the base class
Animal genericAnimal = new Animal("Generic Animal", 5);
genericAnimal.eat(); // "Generic Animal is eating."

// Create an instance of the derived class
Dog buddy = new Dog("Buddy", 3, "Golden Retriever");
buddy.eat(); // "Buddy the Golden Retriever is eating dog food."
buddy.sleep(); // "Buddy is sleeping." (Inherited from Animal)
buddy.bark(); // "Buddy says: Woof Woof!" (Specific to Dog)

// Polymorphism: A Dog IS-A Animal
Animal animal = new Dog("Max", 2, "German Shepherd");
animal.eat(); // "Max the German Shepherd is eating dog food."
// animal.bark(); // Error: Animal reference doesn't know about bark method
```

### Polymorphism

Polymorphism allows objects to be treated as instances of their parent class rather than their actual class. It enables one interface to be used for general classes of actions.

#### Method Overriding (Runtime Polymorphism)

```java
// Base class
class Shape {
    public double getArea() {
        return 0; // Default implementation
    }
    
    public void display() {
        System.out.println("This is a shape");
    }
}

// Derived class 1
class Circle extends Shape {
    private double radius;
    
    public Circle(double radius) {
        this.radius = radius;
    }
    
    @Override
    public double getArea() {
        return Math.PI * radius * radius;
    }
    
    @Override
    public void display() {
        System.out.println("This is a circle with radius " + radius);
    }
}

// Derived class 2
class Rectangle extends Shape {
    private double width;
    private double height;
    
    public Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }
    
    @Override
    public double getArea() {
        return width * height;
    }
    
    @Override
    public void display() {
        System.out.println("This is a rectangle with width " + width + " and height " + height);
    }
}
```

#### Using Polymorphism
```java
// Create an array of shapes
Shape[] shapes = new Shape[3];
shapes[0] = new Circle(5.0);
shapes[1] = new Rectangle(4.0, 6.0);
shapes[2] = new Circle(3.0);

// Process shapes polymorphically
for (Shape shape : shapes) {
    shape.display(); // Different implementation called based on actual object type
    System.out.println("Area: " + shape.getArea());
    System.out.println("------------------------");
}
```

#### Method Overloading (Compile-time Polymorphism)
```java
class Calculator {
    // Method with two int parameters
    public int add(int a, int b) {
        return a + b;
    }
    
    // Overloaded method with three int parameters
    public int add(int a, int b, int c) {
        return a + b + c;
    }
    
    // Overloaded method with two double parameters
    public double add(double a, double b) {
        return a + b;
    }
}

// Using overloaded methods
Calculator calc = new Calculator();
int sum1 = calc.add(5, 3); // Calls the first method
int sum2 = calc.add(5, 3, 2); // Calls the second method
double sum3 = calc.add(5.5, 3.5); // Calls the third method
```

### Abstraction

Abstraction is the concept of hiding complex implementation details and showing only the necessary features of an object. It's achieved through abstract classes and interfaces.

#### Abstract Classes
```java
// Abstract class
abstract class Vehicle {
    private String brand;
    
    public Vehicle(String brand) {
        this.brand = brand;
    }
    
    // Abstract method (must be implemented by concrete subclasses)
    public abstract void drive();
    
    // Concrete method
    public void startEngine() {
        System.out.println("Engine of " + brand + " started.");
    }
    
    public String getBrand() {
        return brand;
    }
}

// Concrete subclass
class Car extends Vehicle {
    public Car(String brand) {
        super(brand);
    }
    
    // Implementing the abstract method
    @Override
    public void drive() {
        System.out.println(getBrand() + " car is driving on the road.");
    }
    
    // Additional method specific to Car
    public void honk() {
        System.out.println("Beep beep!");
    }
}

// Another concrete subclass
class Motorcycle extends Vehicle {
    public Motorcycle(String brand) {
        super(brand);
    }
    
    // Implementing the abstract method
    @Override
    public void drive() {
        System.out.println(getBrand() + " motorcycle is racing on the track.");
    }
    
    // Additional method specific to Motorcycle
    public void wheelie() {
        System.out.println("Doing a wheelie!");
    }
}
```

#### Using Abstract Classes
```java
// Cannot instantiate an abstract class
// Vehicle vehicle = new Vehicle("Generic"); // Error

// Create instances of concrete classes
Car car = new Car("Toyota");
Motorcycle motorcycle = new Motorcycle("Harley-Davidson");

// Using methods
car.startEngine(); // "Engine of Toyota started."
car.drive(); // "Toyota car is driving on the road."
car.honk(); // "Beep beep!"

motorcycle.startEngine(); // "Engine of Harley-Davidson started."
motorcycle.drive(); // "Harley-Davidson motorcycle is racing on the track."
motorcycle.wheelie(); // "Doing a wheelie!"

// Polymorphic usage with abstract type
Vehicle vehicle = car;
vehicle.drive(); // "Toyota car is driving on the road."
// vehicle.honk(); // Error: Vehicle reference doesn't know about honk method
```

### Interfaces

An interface is a completely abstract type that contains only abstract method signatures and constants. It establishes a contract for classes to implement.

#### Defining Interfaces
```java
// Interface definition
interface Drawable {
    void draw(); // Abstract method (implicitly public and abstract)
    
    // Default method (introduced in Java 8)
    default void display() {
        System.out.println("Displaying drawable object");
    }
    
    // Static method (introduced in Java 8)
    static String getInfo() {
        return "Drawable objects can be drawn";
    }
}

// Another interface
interface Resizable {
    void resize(double factor);
}

// Class implementing a single interface
class Circle implements Drawable {
    private double radius;
    
    public Circle(double radius) {
        this.radius = radius;
    }
    
    @Override
    public void draw() {
        System.out.println("Drawing a circle with radius " + radius);
    }
}

// Class implementing multiple interfaces
class Rectangle implements Drawable, Resizable {
    private double width;
    private double height;
    
    public Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }
    
    @Override
    public void draw() {
        System.out.println("Drawing a rectangle with width " + width + " and height " + height);
    }
    
    @Override
    public void resize(double factor) {
        width *= factor;
        height *= factor;
        System.out.println("Resized to width " + width + " and height " + height);
    }
}
```

#### Using Interfaces
```java
// Create objects
Circle circle = new Circle(5.0);
Rectangle rectangle = new Rectangle(4.0, 6.0);

// Call implemented methods
circle.draw(); // "Drawing a circle with radius 5.0"
circle.display(); // "Displaying drawable object" (default method)

rectangle.draw(); // "Drawing a rectangle with width 4.0 and height 6.0"
rectangle.resize(1.5); // "Resized to width 6.0 and height 9.0"

// Polymorphism with interfaces
Drawable drawable1 = circle;
Drawable drawable2 = rectangle;
drawable1.draw(); // "Drawing a circle with radius 5.0"
drawable2.draw(); // "Drawing a rectangle with width 6.0 and height 9.0"

// Static method call on interface
System.out.println(Drawable.getInfo()); // "Drawable objects can be drawn"
```

### Practice Exercises: Object-Oriented Programming

#### Exercise 1: Bank Account System
Create a banking system with:
1. An abstract `Account` class with:
   - Balance and account number
   - Methods for deposit, withdraw, and getBalance
2. Two concrete classes extending Account:
   - `SavingsAccount` with interest rate functionality
   - `CheckingAccount` with transaction fee functionality
3. A `Bank` class that can hold multiple accounts and perform operations across them

#### Exercise 2: Shape Hierarchy
Create:
1. A `Shape` interface with methods for area and perimeter
2. Classes implementing Shape: `Circle`, `Rectangle`, `Triangle`
3. A class to demonstrate polymorphism by processing different shapes

891
