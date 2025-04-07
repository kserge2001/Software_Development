# Go Programming: A Comprehensive Guide

## Table of Contents
- [Introduction to Go](#introduction-to-go)
- [Setting Up Go Development Environment](#setting-up-go-development-environment)
- [Basic Syntax and Data Types](#basic-syntax-and-data-types)
- [Control Flow and Functions](#control-flow-and-functions)
- [Packages and Modules](#packages-and-modules)
- [Structs and Interfaces](#structs-and-interfaces)
- [Concurrency with Goroutines and Channels](#concurrency-with-goroutines-and-channels)
- [Error Handling](#error-handling)
- [Testing in Go](#testing-in-go)
- [Standard Library Overview](#standard-library-overview)
- [Web Development with Go](#web-development-with-go)
- [Database Access](#database-access)
- [Best Practices](#best-practices)
- [Common Design Patterns](#common-design-patterns)
- [Real-World Project Examples](#real-world-project-examples)
- [Additional Resources](#additional-resources)

## Introduction to Go

### What is Go?

Go (or Golang) is an open-source programming language created by Google in 2007 and officially announced in 2009. It was designed by Robert Griesemer, Rob Pike, and Ken Thompson with the goal of creating a language that is efficient, readable, and safe.

### Key Features of Go

- **Simplicity and Readability**: Minimalist syntax with few keywords
- **Static Typing**: Strong typing with type inference
- **Compiled Language**: Compiles directly to machine code for efficiency
- **Fast Compilation**: Designed for quick build times
- **Garbage Collection**: Automatic memory management
- **Built-in Concurrency**: Goroutines and channels make concurrent programming easier
- **Cross-Platform**: Compile for different operating systems easily
- **Standard Library**: Rich standard library that covers many common needs
- **Open Source**: Community-driven development and improvements

### The Philosophy Behind Go

Go was designed with a strong philosophy in mind:

1. **Simplicity over complexity**: Fewer features, but each one well-designed
2. **Explicitness over implicitness**: Code should be clear and obvious
3. **Composition over inheritance**: Build complex types by combining simpler ones
4. **Concurrency as a first-class citizen**: Built into the language, not an afterthought
5. **Practicality over theory**: Focusing on solving real-world problems efficiently

### Use Cases for Go

Go excels in several domains:

- **Cloud and Network Services**: Used by many cloud providers and for microservices
- **Web Development**: Building APIs and web applications
- **DevOps Tools**: Docker, Kubernetes, and many CI/CD tools are written in Go
- **Command-Line Applications**: Fast and efficient CLI tools
- **Distributed Systems**: Systems that need to handle concurrency well
- **High-Performance Computing**: When you need speed and efficiency

### Go vs Other Languages

- **Go vs Java**: Simpler syntax, faster compile times, but less OOP features
- **Go vs Python**: Much faster, statically typed, but less flexibility
- **Go vs C/C++**: Safer memory management, simpler syntax, but sometimes less performant
- **Go vs Rust**: Easier to learn, garbage collection, but less memory control

### Practice Exercise: Understanding Go's Place in Software Development

1. Research and list three significant software systems built with Go
2. Compare Go with a language you're familiar with, noting at least three differences
3. Explain why Go might be a good choice for a specific type of application

## Setting Up Go Development Environment

### Installing Go

#### Windows

1. Download the MSI installer from [golang.org](https://golang.org/dl/)
2. Run the installer and follow the prompts
3. Verify installation by opening Command Prompt and typing `go version`

#### macOS

Using Homebrew (recommended):
```bash
brew install go
```

Or download the package installer from the official website.

#### Linux

```bash
# Ubuntu/Debian
sudo apt update
sudo apt install golang-go

# Fedora
sudo dnf install golang

# Arch Linux
sudo pacman -S go
```

### Configuring Your Go Workspace

Go code is typically organized in a specific workspace structure:

```
$HOME/go/
├── bin/    # Compiled binaries
├── pkg/    # Package objects
└── src/    # Source code
```

Set up your environment variables:

```bash
# Add these to your .bashrc, .zshrc, or equivalent
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```

> **Note**: With Go Modules (Go 1.11+), you can create projects outside of GOPATH.

### Go Development Tools

#### Text Editors and IDEs

- **Visual Studio Code** with Go extension (highly recommended)
- **GoLand** by JetBrains (commercial)
- **Vim/Neovim** with vim-go plugin
- **Sublime Text** with GoSublime
- **Atom** with go-plus package

#### Setting Up VSCode for Go Development

1. Install Visual Studio Code
2. Install the Go extension
3. Open VS Code settings and configure Go settings:
   ```json
   {
       "go.useLanguageServer": true,
       "go.formatTool": "goimports",
       "go.lintTool": "golangci-lint",
       "editor.formatOnSave": true
   }
   ```
4. Install Go tools by pressing `Ctrl+Shift+P` or `Cmd+Shift+P` and typing "Go: Install/Update Tools"

### Essential Go Tools

```bash
# Install essential Go tools
go install golang.org/x/tools/cmd/goimports@latest
go install golang.org/x/lint/golint@latest
go install github.com/golangci/golangci-lint/cmd/golangci-lint@latest
go install github.com/go-delve/delve/cmd/dlv@latest
go install honnef.co/go/tools/cmd/staticcheck@latest
```

### Hello World in Go

Create a file named `hello.go`:

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

Run the program:

```bash
go run hello.go
```

Build an executable:

```bash
go build hello.go
./hello  # Run the executable
```

### Go Commands

```bash
go help           # Shows help information
go run file.go    # Compiles and runs a program
go build          # Compiles packages and dependencies
go install        # Compiles and installs packages
go test           # Tests packages
go get            # Downloads and installs packages
go mod init       # Initializes a new module
go mod tidy       # Adds missing and removes unused modules
go fmt            # Formats Go source code
go doc            # Shows documentation for a package
```

### Practice Exercise: Setting Up Your Go Environment

1. Install Go on your system and verify the installation
2. Set up your Go workspace and environment variables
3. Create, run, and build a simple "Hello, World!" program
4. Modify the program to print your name and run it again
5. Install the essential Go tools mentioned above

## Basic Syntax and Data Types

### Program Structure

A typical Go program consists of:

```go
// Package declaration
package main

// Import statements
import (
    "fmt"
    "math"
)

// Constants
const Pi = 3.14159

// Variables
var (
    name    = "John"
    age     = 30
    isValid = true
)

// Function declaration
func add(x, y int) int {
    return x + y
}

// Main function - entry point
func main() {
    // Local variables
    result := add(5, 3)
    fmt.Println("Result:", result)
    
    // Control structures, etc.
}
```

### Comments

```go
// This is a single-line comment

/*
This is a
multi-line comment
*/
```

### Variables and Declaration

```go
// Explicit declaration
var name string = "John"
var age int = 30
var isValid bool = true

// Type inference
var city = "New York"  // string type is inferred
var population = 8000000  // int type is inferred

// Short declaration (only inside functions)
func main() {
    count := 10  // Shorthand for var count = 10
    message := "Hello"
    
    // Multiple declarations
    width, height := 100, 50
    
    // Redeclaration (at least one variable must be new)
    width, unit := 120, "px"  // unit is new
}
```

### Constants

```go
// Typed constants
const Pi float64 = 3.14159
const MaxConnections int = 1000

// Untyped constants
const (
    StatusOK       = 200
    StatusNotFound = 404
    Company        = "Acme Corp"
)

// Iota for enumerated constants
const (
    Sunday = iota  // 0
    Monday         // 1
    Tuesday        // 2
    Wednesday      // 3
    Thursday       // 4
    Friday         // 5
    Saturday       // 6
)

// Iota with expressions
const (
    _           = iota  // ignore first value
    KB ByteSize = 1 << (10 * iota)  // 1 << 10 = 1024
    MB                              // 1 << 20
    GB                              // 1 << 30
    TB                              // 1 << 40
)
```

### Basic Data Types

#### Numeric Types

```go
// Integer types
var a int = 10          // platform-dependent size (32 or 64 bit)
var b int8 = 127        // -128 to 127
var c int16 = 32767     // -32768 to 32767
var d int32 = 2147483647  // -2^31 to 2^31-1
var e int64 = 9223372036854775807  // -2^63 to 2^63-1

// Unsigned integer types
var f uint = 10         // platform-dependent size
var g uint8 = 255       // 0 to 255
var h uint16 = 65535    // 0 to 65535
var i uint32 = 4294967295  // 0 to 2^32-1
var j uint64 = 18446744073709551615  // 0 to 2^64-1

// Special integer types
var k byte = 255        // alias for uint8
var l rune = 'A'        // alias for int32, represents a Unicode code point

// Floating-point types
var m float32 = 3.14    // IEEE-754 32-bit floating-point
var n float64 = 3.14159265359  // IEEE-754 64-bit floating-point

// Complex types
var o complex64 = 1 + 2i   // complex numbers with float32 real and imaginary parts
var p complex128 = 3.0 + 4.0i  // complex numbers with float64 real and imaginary parts
```

#### Boolean Type

```go
var isEnabled bool = true
var isFinished bool = false

// Zero value is false
var isReady bool  // defaults to false
```

#### String Type

```go
var greeting string = "Hello, World!"
var multiline string = `This is a
multi-line
string`

// String operations
name := "Go Programming"
firstChar := name[0]        // 'G' (byte, not string)
length := len(name)         // 14
substring := name[0:2]      // "Go"
concatenated := "Hello, " + name  // "Hello, Go Programming"

// Iterating over a string
for i, char := range "Hello" {
    fmt.Printf("Character at position %d: %c\n", i, char)
}
```

### Composite Types

#### Arrays

```go
// Fixed-size array declaration
var numbers [5]int  // Array of 5 integers, initialized to zeros

// Array initialization
vowels := [5]string{"a", "e", "i", "o", "u"}
daysOfWeek := [...]string{"Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"}  // Size determined by elements

// Accessing elements
first := vowels[0]  // "a"
vowels[1] = "E"     // Modify element

// Iterating over an array
for i, v := range vowels {
    fmt.Printf("Index: %d, Value: %s\n", i, v)
}

// Array length
size := len(vowels)  // 5

// Multi-dimensional arrays
var matrix [3][4]int  // 3x4 matrix
matrix[0][0] = 1      // Set element at row 0, column 0
```

#### Slices

Slices are more flexible than arrays and are used more frequently in Go programs.

```go
// Slice declaration
var scores []int  // nil slice, length 0, capacity 0

// Slice creation
numbers := []int{1, 2, 3, 4, 5}  // Slice literal
names := make([]string, 3)       // Slice with length 3, capacity 3
buffer := make([]byte, 10, 100)  // Slice with length 10, capacity 100

// Slice from array
arr := [5]int{10, 20, 30, 40, 50}
slice1 := arr[1:4]  // [20, 30, 40]
slice2 := arr[:3]   // [10, 20, 30]
slice3 := arr[2:]   // [30, 40, 50]
slice4 := arr[:]    // [10, 20, 30, 40, 50]

// Adding elements
numbers = append(numbers, 6)          // Add one element
numbers = append(numbers, 7, 8, 9)    // Add multiple elements
combined := append(numbers, slice1...) // Append a slice

// Slice length and capacity
length := len(numbers)     // Number of elements
capacity := cap(numbers)   // Underlying array size

// Copying slices
dest := make([]int, len(numbers))
copied := copy(dest, numbers)  // Returns number of elements copied

// Slicing a slice
sub := numbers[2:5]  // Creates a new slice that references the same array

// Iterating over a slice
for i, v := range numbers {
    fmt.Printf("Index: %d, Value: %d\n", i, v)
}
```

#### Maps

```go
// Map declaration
var ages map[string]int  // nil map

// Map creation
salaries := map[string]float64{
    "John": 50000.0,
    "Jane": 60000.0,
    "Bob":  55000.0,
}

employees := make(map[string]int)  // Empty map

// Adding and updating entries
employees["Alice"] = 101
employees["Bob"] = 102
employees["Alice"] = 103  // Update

// Retrieving values
salary := salaries["John"]  // 50000.0
id, exists := employees["Charlie"]  // id=0, exists=false (zero value if key doesn't exist)

// Checking if a key exists
if val, ok := salaries["Jane"]; ok {
    fmt.Printf("Jane's salary: %.2f\n", val)
}

// Deleting entries
delete(employees, "Bob")

// Map length
size := len(salaries)  // 3

// Iterating over a map
for name, salary := range salaries {
    fmt.Printf("%s earns %.2f\n", name, salary)
}
```

### Zero Values

In Go, variables are always initialized with a type-specific zero value if not explicitly initialized:

```go
var i int        // 0
var f float64    // 0.0
var b bool       // false
var s string     // "" (empty string)
var p *int       // nil (zero value for pointers)
var slice []int  // nil (zero value for slices)
var m map[string]int // nil (zero value for maps)
var c chan int   // nil (zero value for channels)
var e error      // nil (zero value for interfaces)
```

### Type Conversion

Go requires explicit type conversion:

```go
var i int = 42
var f float64 = float64(i)  // int to float64
var u uint = uint(f)        // float64 to uint

// Converting between strings and numbers
import "strconv"

// String to int
s := "123"
i, err := strconv.Atoi(s)  // i = 123, err = nil

// Int to string
i = 456
s = strconv.Itoa(i)  // s = "456"

// String to float
s = "3.14"
f, err := strconv.ParseFloat(s, 64)  // f = 3.14, err = nil

// Float to string
f = 3.14159
s = strconv.FormatFloat(f, 'f', 2, 64)  // s = "3.14"
```

### Practice Exercise: Data Types and Variables

1. Create a program that demonstrates each of Go's basic data types
2. Write a function that converts between different numeric types and prints the results
3. Create a program that manipulates strings, arrays, slices, and maps
4. Implement a function that demonstrates type conversions in various scenarios

## Control Flow and Functions

### Conditional Statements

#### if Statement

```go
// Basic if statement
if x > 10 {
    fmt.Println("x is greater than 10")
}

// if with initialization statement
if age := getAge(); age >= 18 {
    fmt.Println("Adult")
} else {
    fmt.Println("Minor")
}
// Note: 'age' is only in scope within the if/else blocks

// if-else chain
if score >= 90 {
    fmt.Println("A")
} else if score >= 80 {
    fmt.Println("B")
} else if score >= 70 {
    fmt.Println("C")
} else {
    fmt.Println("F")
}
```

#### switch Statement

```go
// Basic switch
day := "Monday"
switch day {
case "Monday":
    fmt.Println("Start of work week")
case "Tuesday", "Wednesday", "Thursday":
    fmt.Println("Midweek")
case "Friday":
    fmt.Println("End of work week")
case "Saturday", "Sunday":
    fmt.Println("Weekend")
default:
    fmt.Println("Invalid day")
}

// Switch with initialization
switch os := runtime.GOOS; os {
case "darwin":
    fmt.Println("macOS")
case "linux":
    fmt.Println("Linux")
case "windows":
    fmt.Println("Windows")
default:
    fmt.Printf("%s\n", os)
}

// Switch without expression (like if-else chain)
switch {
case time.Now().Hour() < 12:
    fmt.Println("Good morning")
case time.Now().Hour() < 17:
    fmt.Println("Good afternoon")
default:
    fmt.Println("Good evening")
}

// Switch with fallthrough (uncommon)
switch num := 4; num {
case 1:
    fmt.Println("One")
case 2:
    fmt.Println("Two")
    fallthrough // Executes the next case regardless of its condition
case 3:
    fmt.Println("Three or more")
case 4:
    fmt.Println("Four or more")
}
// Prints: "Four or more"
```

### Loops

Go has only one loop construct: the `for` loop.

```go
// Basic for loop
for i := 0; i < 5; i++ {
    fmt.Println(i)
}

// For loop as a while loop
i := 0
for i < 5 {
    fmt.Println(i)
    i++
}

// Infinite loop with break
for {
    fmt.Println("Infinite loop")
    break // Exit the loop
}

// For loop with continue
for i := 0; i < 10; i++ {
    if i%2 == 0 {
        continue // Skip even numbers
    }
    fmt.Println(i) // Prints odd numbers
}

// For loop with range
// For arrays, slices, strings
fruits := []string{"apple", "banana", "cherry"}
for i, fruit := range fruits {
    fmt.Printf("Index: %d, Value: %s\n", i, fruit)
}

// For maps
ages := map[string]int{"Alice": 25, "Bob": 30, "Charlie": 22}
for name, age := range ages {
    fmt.Printf("%s is %d years old\n", name, age)
}

// Using only the index/key
for i := range fruits {
    fmt.Printf("Fruit at index %d\n", i)
}

// Using only the value (blank identifier for index)
for _, fruit := range fruits {
    fmt.Println(fruit)
}
```

### Practice Exercise: Control Flow

1. Write a program that prints FizzBuzz (divisible by 3: "Fizz", divisible by 5: "Buzz", both: "FizzBuzz")
2. Create a simple calculator program using switch statements
3. Write a program that finds prime numbers up to n using loops and conditionals
4. Implement a binary search algorithm using loops

### Functions

#### Basic Function Declaration

```go
// Function with parameters and a return value
func add(a, b int) int {
    return a + b
}

// Function with named return value
func subtract(a, b int) (result int) {
    result = a - b
    return // Automatically returns the named variable 'result'
}

// Function with no parameters or return value
func printHello() {
    fmt.Println("Hello, World!")
}

// Function with no return value
func printSum(a, b int) {
    fmt.Printf("%d + %d = %d\n", a, b, a+b)
}
```

#### Multiple Return Values

```go
// Function returning multiple values
func divideAndRemainder(dividend, divisor int) (int, int, error) {
    if divisor == 0 {
        return 0, 0, errors.New("division by zero")
    }
    return dividend / divisor, dividend % divisor, nil
}

// Using multiple return values
quotient, remainder, err := divideAndRemainder(10, 3)
if err != nil {
    fmt.Println("Error:", err)
    return
}
fmt.Printf("Quotient: %d, Remainder: %d\n", quotient, remainder)

// Ignoring some return values with blank identifier
quotient, _, err = divideAndRemainder(10, 3)
```

#### Variadic Functions

```go
// Function with variable number of arguments
func sum(nums ...int) int {
    total := 0
    for _, num := range nums {
        total += num
    }
    return total
}

// Calling variadic functions
result1 := sum(1, 2)           // 3
result2 := sum(1, 2, 3, 4, 5)  // 15

// Passing a slice to a variadic function
numbers := []int{1, 2, 3, 4, 5}
result3 := sum(numbers...)  // 15
```

#### Closures and Anonymous Functions

```go
// Anonymous function assigned to a variable
add := func(a, b int) int {
    return a + b
}
result := add(3, 4)  // 7

// Immediate invocation
result2 := func(a, b int) int {
    return a * b
}(3, 4)  // 12

// Closure capturing outer variables
func makeCounter() func() int {
    count := 0
    return func() int {
        count++
        return count
    }
}

counter1 := makeCounter()
fmt.Println(counter1())  // 1
fmt.Println(counter1())  // 2

counter2 := makeCounter()
fmt.Println(counter2())  // 1 (independent counter)
```

#### Defer

```go
// Deferred function calls are executed when the surrounding function returns
func processFile(filename string) error {
    file, err := os.Open(filename)
    if err != nil {
        return err
    }
    defer file.Close()  // Will be executed when processFile returns
    
    // Process the file...
    return nil
}

// Multiple defers are executed in LIFO order (last in, first out)
func multipleDefers() {
    fmt.Println("Start")
    defer fmt.Println("This runs last")
    defer fmt.Println("This runs second")
    defer fmt.Println("This runs first")
    fmt.Println("End")
}
// Output:
// Start
// End
// This runs first
// This runs second
// This runs last
```

#### Function as Values and Types

```go
// Function type declaration
type MathFunc func(int, int) int

// Function that takes a function as an argument
func calculate(a, b int, operation MathFunc) int {
    return operation(a, b)
}

// Functions to pass as arguments
func add(a, b int) int {
    return a + b
}

func multiply(a, b int) int {
    return a * b
}

// Using function values
result1 := calculate(5, 3, add)       // 8
result2 := calculate(5, 3, multiply)  // 15
```

### Practice Exercise: Functions

1. Write a function that accepts a variable number of strings and returns their concatenation
2. Create a function that returns multiple values (e.g., a function that finds the min, max, and avg of a slice of numbers)
3. Implement a higher-order function that takes a function as an argument
4. Write a function that uses defer to ensure resources are properly released
5. Create a closure that maintains state between function calls

## Concurrency with Goroutines and Channels

### Goroutines

Goroutines are lightweight threads managed by the Go runtime.

```go
// Basic goroutine
func sayHello() {
    fmt.Println("Hello, World!")
}

func main() {
    // Start a goroutine
    go sayHello()
    
    // Direct call to anonymous function as goroutine
    go func() {
        fmt.Println("Hello from anonymous function")
    }()
    
    // Give goroutines time to execute before main function exits
    time.Sleep(100 * time.Millisecond)
}
```

### Channels

Channels are the pipes that connect concurrent goroutines.

```go
// Creating a channel
ch := make(chan int)      // Unbuffered channel
ch2 := make(chan int, 10) // Buffered channel with capacity 10

// Sending on a channel
ch <- 42

// Receiving from a channel
value := <-ch

// Closing a channel
close(ch)

// Check if a channel is closed
value, ok := <-ch  // ok is false if channel is closed
```

#### Channel Operations

```go
// Simple channel example
func sum(s []int, c chan int) {
    sum := 0
    for _, v := range s {
        sum += v
    }
    c <- sum // Send sum to channel
}
func main() {
    s := []int{7, 2, 8, -9, 4, 0}
    
    c := make(chan int)
    
    // Split the slice in half and compute partial sums in parallel
    go sum(s[:len(s)/2], c)
    go sum(s[len(s)/2:], c)
    
    // Receive from channel
    x, y := <-c, <-c
    
    fmt.Println(x, y, x+y) // -5, 6, 1 (order of x and y may vary)
}
```

#### Buffered Channels

```go
// Creating a buffered channel
ch := make(chan int, 2) // Buffer size of 2

// Sending values to buffered channel
ch <- 1
ch <- 2
// ch <- 3 // This would block until someone receives from the channel

// Receiving values
fmt.Println(<-ch) // 1
fmt.Println(<-ch) // 2
```

#### Channel Direction

```go
// Function that only receives from a channel
func receive(ch <-chan int) {
    value := <-ch
    fmt.Println("Received:", value)
}

// Function that only sends to a channel
func send(ch chan<- int) {
    ch <- 42
}

func main() {
    ch := make(chan int)
    go send(ch)
    receive(ch)
}
```

#### Ranging and Closing Channels

```go
func fibonacci(n int, c chan int) {
    x, y := 0, 1
    for i := 0; i < n; i++ {
        c <- x
        x, y = y, x+y
    }
    close(c) // Close channel when done sending
}

func main() {
    c := make(chan int, 10)
    go fibonacci(cap(c), c)
    
    // Range over channel values until it's closed
    for i := range c {
        fmt.Println(i)
    }
}
```

### Select Statement

The select statement lets a goroutine wait on multiple communication operations.

```go
func fibonacci(c, quit chan int) {
    x, y := 0, 1
    for {
        select {
        case c <- x:
            x, y = y, x+y
        case <-quit:
            fmt.Println("Quit")
            return
        }
    }
}

func main() {
    c := make(chan int)
    quit := make(chan int)
    
    go func() {
        for i := 0; i < 10; i++ {
            fmt.Println(<-c)
        }
        quit <- 0
    }()
    
    fibonacci(c, quit)
}
```

#### Timeout with Select

```go
func main() {
    c := make(chan int)
    
    go func() {
        time.Sleep(2 * time.Second)
        c <- 42
    }()
    
    select {
    case result := <-c:
        fmt.Println("Result:", result)
    case <-time.After(1 * time.Second):
        fmt.Println("Timed out")
    }
}
```

#### Default Case in Select

```go
func main() {
    tick := time.Tick(100 * time.Millisecond)
    boom := time.After(500 * time.Millisecond)
    
    for {
        select {
        case <-tick:
            fmt.Println("Tick")
        case <-boom:
            fmt.Println("Boom!")
            return
        default:
            fmt.Println("    .")
            time.Sleep(50 * time.Millisecond)
        }
    }
}
```

### Concurrency Patterns

#### Worker Pools

```go
func worker(id int, jobs <-chan int, results chan<- int) {
    for j := range jobs {
        fmt.Printf("Worker %d started job %d\n", id, j)
        time.Sleep(time.Second) // Simulate work
        fmt.Printf("Worker %d finished job %d\n", id, j)
        results <- j * 2
    }
}

func main() {
    const numJobs = 5
    const numWorkers = 3
    
    jobs := make(chan int, numJobs)
    results := make(chan int, numJobs)
    
    // Start workers
    for w := 1; w <= numWorkers; w++ {
        go worker(w, jobs, results)
    }
    
    // Send jobs
    for j := 1; j <= numJobs; j++ {
        jobs <- j
    }
    close(jobs)
    
    // Collect results
    for a := 1; a <= numJobs; a++ {
        <-results
    }
}
```

#### Fan-out, Fan-in

```go
func producer(nums ...int) <-chan int {
    out := make(chan int)
    go func() {
        defer close(out)
        for _, n := range nums {
            out <- n
        }
    }()
    return out
}

func square(in <-chan int) <-chan int {
    out := make(chan int)
    go func() {
        defer close(out)
        for n := range in {
            out <- n * n
        }
    }()
    return out
}

func merge(cs ...<-chan int) <-chan int {
    var wg sync.WaitGroup
    out := make(chan int)
    
    // Start an output goroutine for each input channel
    output := func(c <-chan int) {
        defer wg.Done()
        for n := range c {
            out <- n
        }
    }
    
    wg.Add(len(cs))
    for _, c := range cs {
        go output(c)
    }
    
    // Start a goroutine to close out once all the output goroutines are done
    go func() {
        wg.Wait()
        close(out)
    }()
    
    return out
}

func main() {
    in := producer(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
    
    // Fan out to 3 square operations
    c1 := square(in)
    c2 := square(in)
    c3 := square(in)
    
    // Fan in the results
    for n := range merge(c1, c2, c3) {
        fmt.Println(n)
    }
}
```

### Practice Exercise: Concurrency

1. Create a program that runs multiple goroutines to compute a result
2. Implement a worker pool with a specified number of workers
3. Use select to wait on multiple channels with a timeout
4. Build a pipeline of goroutines that processes data in stages
5. Implement a concurrent web scraper that fetches and processes multiple URLs in parallel

## Error Handling

### Basic Error Handling

```go
// Function that returns an error
func divide(a, b float64) (float64, error) {
    if b == 0 {
        return 0, errors.New("division by zero")
    }
    return a / b, nil
}

// Using the error
func main() {
    result, err := divide(10, 0)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Result:", result)
}
```

### Custom Error Types

```go
// Custom error type
type DivisionError struct {
    Dividend float64
    Divisor  float64
    Message  string
}

// Implement the Error interface
func (e *DivisionError) Error() string {
    return fmt.Sprintf("%s: %f / %f", e.Message, e.Dividend, e.Divisor)
}

// Function returning custom error
func divide(a, b float64) (float64, error) {
    if b == 0 {
        return 0, &DivisionError{
            Dividend: a,
            Divisor:  b,
            Message:  "division by zero",
        }
    }
    return a / b, nil
}

// Using and checking for custom error
func main() {
    result, err := divide(10, 0)
    if err != nil {
        if divErr, ok := err.(*DivisionError); ok {
            fmt.Printf("Custom error: %v\n", divErr)
        } else {
            fmt.Println("Other error:", err)
        }
        return
    }
    fmt.Println("Result:", result)
}
```

### Multiple Error Values

```go
// Use fmt.Errorf to combine errors
func fileChecker(name string) error {
    if name == "" {
        return fmt.Errorf("filename cannot be empty")
    }
    if len(name) < 3 {
        return fmt.Errorf("filename %s is too short", name)
    }
    return nil
}

// Wrap errors with additional context
func openFile(path string) (*os.File, error) {
    err := fileChecker(path)
    if err != nil {
        return nil, fmt.Errorf("file check failed: %w", err)
    }
    
    f, err := os.Open(path)
    if err != nil {
        return nil, fmt.Errorf("open operation failed: %w", err)
    }
    return f, nil
}

// Unwrapping errors (Go 1.13+)
func main() {
    file, err := openFile("a")
    if err != nil {
        fmt.Println(err) // Full error chain
        
        // Unwrap to check the original error
        if errors.Is(err, os.ErrNotExist) {
            fmt.Println("File does not exist")
        }
        
        var pathError *os.PathError
        if errors.As(err, &pathError) {
            fmt.Printf("Path error: %v\n", pathError.Path)
        }
    } else {
        defer file.Close()
        // Use the file
    }
}
```

### Panic and Recover

```go
// Panic stops normal execution
func doPanic() {
    fmt.Println("About to panic")
    panic("something bad happened")
    // Code after panic is not executed
    fmt.Println("After panic") // Never reached
}

// Recover can catch a panic
func recoverExample() {
    defer func() {
        if r := recover(); r != nil {
            fmt.Println("Recovered from:", r)
        }
    }()
    
    doPanic()
    
    // Code after a recovered panic resumes
    fmt.Println("After recover") // This is not reached
}

func main() {
    recoverExample()
    fmt.Println("Program continues") // This is executed
}
```
1
