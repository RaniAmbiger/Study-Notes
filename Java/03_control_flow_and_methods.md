## 18. Conditional Statements in Java

Conditional statements are used to perform different actions based on different conditions. They help in decision-making in a program by controlling the flow of execution.

---

## 1. if Statement

The `if` statement allows you to execute a block of code only if a specified condition is true.

### Syntax 

```java
if (condition) {
    // code to execute if condition is true
}
```
### Example

```java
int number = 10;
if (number > 0) {
    System.out.println("The number is positive.");//The number is positive.
}
```
---

## 2. if-else Statement

The `if-else` statement executes one block of code if the condition is true, otherwise it executes another block.

### Syntax

```java
if (condition) {
    // code to execute if condition is true
} else {
    // code to execute if condition is false
}
```
### Example

```java
int number = -5;
if (number > 0) {
    System.out.println("The number is positive.");
} else {
    System.out.println("The number is not positive.");//The number is not positive.
}
```
---

## 3. if-else-if Ladder

The `if-else-if` ladder is used to test multiple conditions sequentially. The first true condition’s block is executed.

### Syntax

```java
if (condition1) {
    // code if condition1 is true
} else if (condition2) {
    // code if condition2 is true
} else if (condition3) {
    // code if condition3 is true
} else {
    // code if none of the above conditions are true
}
```
### Example

```java
int marks = 75;

if (marks >= 90) {
    System.out.println("Grade A");
} else if (marks >= 75) {
    System.out.println("Grade B");//Grade B
} else if (marks >= 50) {
    System.out.println("Grade C");
} else {
    System.out.println("Fail");
}
```
---

## 4. Nested if Statement

A nested `if` statement is an `if` or `if-else` statement inside another `if` or `else` block.

### Syntax

```java
if (condition1) {
    if (condition2) {
        // code if both condition1 and condition2 are true
    } else {
        // code if condition1 is true but condition2 is false
    }
} else {
    // code if condition1 is false
}
```
### Example

```java
int number = 10;

if (number > 0) {
    if (number % 2 == 0) {
        System.out.println("Positive even number");//Positive even number
    } else {
        System.out.println("Positive odd number");
    }
} else {
    System.out.println("Number is not positive");
}
```
---

## 5. switch Statement

The `switch` statement allows selection among multiple options based on the value of an expression.

### Syntax

```java
switch (expression) {
    case value1:
        // code to execute if expression == value1
        break;
    case value2:
        // code to execute if expression == value2
        break;
    // more cases
    default:
        // code to execute if none of the cases match
}
```

### Example

```java
int day = 3;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");//Wednesday
        break;
    default:
        System.out.println("Invalid day");
}
```
---

## 19. Looping Statements in Java

Looping statements are used to execute a block of code repeatedly as long as a specified condition is true.

---

## 1. for Loop

The `for` loop executes a block of code a specific number of times.

### Syntax

```java
for (initialization; condition; update) {
    // code to be executed
}
```
---

### Example

```java
public class ForLoopExample {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
// Output:
// 1
// 2
// 3
// 4
// 5
```
---

## 2. while Loop

The while loop executes a block of code repeatedly as long as the condition is true. The condition is evaluated before entering the loop.

### Syntax

```java
while (condition) {
    // code to be executed
}
```
---

### Example
```java
public class WhileLoopExample {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 5) {
            System.out.println(i);
            i++;
        }
    }
}
// Output:
// 1
// 2
// 3
// 4
// 5
```
---

## 3. do-while Loop

The do-while loop executes the block of code once, then checks the condition and repeats as long as the condition is true.

### Syntax

```java
do {
    // code to be executed
} while (condition);
```
---

### Example

```java
public class DoWhileExample {
    public static void main(String[] args) {
        int i = 1;
        do {
            System.out.println(i);
            i++;
        } while (i <= 5);
    }
}
// Output:
// 1
// 2
// 3
// 4
// 5
```
---

## 4. for-each Loop

The `for-each` loop is used to iterate over elements in arrays or collections. It simplifies the loop when you don't need to know the index.

### Syntax

```java
for (datatype variable : arrayOrCollection) {
    // code to be executed
}
```
---

### example will be coverd in collection framework

---

## 20. Method

A **method** is a block of code that performs a specific task. It helps in code reusability — once a method is written, it can be used many times.

---

## Types of Methods

1. **Predefined Methods** – Already defined in Java libraries (e.g., `System.out.println()`)
2. **User-defined Methods** – Created by the programmer to perform specific tasks.

---

## Syntax

```java
returnType methodName(parameters) {
    // method body
}
```
---
* **returnType**
- The `returnType` specifies what type of value the method will return after execution.
- It can be a **primitive data type** (like `int`, `float`, `boolean`), a **class type** (like `String`, `ArrayList`), or `void` if the method does **not return any value**.
- If the method returns a value, the `return` keyword must be used within the method body to return the appropriate value of the specified type.

---

* **methodName**
- The methodName is the identifier used to call the method.
- It should follow standard naming conventions:
- Start with a lowercase letter.
- Use camelCase for multiple words (e.g., calculateSum).
- It should be descriptive of the method’s purpose.

---

* **parameters**
- Parameters are the values passed to the method to perform operations.
- They are declared within the parentheses after the method name.
- A method can take zero or more parameters, and each parameter must have a defined data type.
- If no parameters are needed, empty parentheses () are used.

---

* **method body** 
- The method body is enclosed in curly braces {}.
- It contains the statements that define what the method will do when called.
- This includes calculations, conditions, loops, print statements, and return values (if any).
- The body must match the logic expected by the method name and parameters.

---

### 🔹 Example 1: Method without Parameters and No Return

```java
public class MethodExample1 {
    public static void greet() {
        System.out.println("Hello, Welcome to Java!");
    }

    public static void main(String[] args) {
        greet(); // Calling the method
    }
}
// Output:
// Hello, Welcome to Java!
```
---

### 🔹 Example 2: Method with Parameters

```java
public class MethodExample2 {
    public static void add(int a, int b) {
        int sum = a + b;
        System.out.println("Sum: " + sum);
    }

    public static void main(String[] args) {
        add(10, 20); // Passing arguments
    }
}
// Output:
// Sum: 30
```
---

### 🔹 Example 3: Method with Return Type

```java
public class MethodExample3 {
    public static int square(int x) {
        return x * x;
    }

    public static void main(String[] args) {
        int result = square(5);
        System.out.println("Square: " + result);
    }
}
// Output:
// Square: 25
```
---

### 🔹 Advantages of Using Methods

* Code Reusability

* Code Readability

* Easy Maintenance

* Modular Approach

---

# 21. Stack Memory

-
-
-
-
-


---

## Java Method Terms Explained

### 1. Actual Argument (Actual Parameter)  
The actual argument is the real value or variable that you pass to a method when calling it.  
These are the inputs provided in the method call.

**Example:**  
```java
obj.sum(5, 10);//Here, 5 and 10 are the actual arguments.
```
---

### 2. Formal Argument (Formal Parameter)  
The formal argument is the variable declared in the method definition that receives the value when the method is called.  
These act as placeholders inside the method to represent the values passed.

**Example:**  
```java
public int sum(int a, int b) //Here, a and b are the formal arguments.
{
    return a + b;
}
```
---

### 3. Method Signature  
The method signature uniquely identifies a method in a class.

It consists of:  
- Method name  
- Parameter list (number, type, and order of parameters)

It does **NOT** include the return type or exceptions.

Java uses the method signature to distinguish between overloaded methods.

**Example:**  
```java
void display(int a, String b)  // Method name = display, Parameters = (int, String)
```
---

### Summary

| Term             | What it means                                    | Example                          |
|------------------|-------------------------------------------------|---------------------------------|
| Actual Argument  | Value/variable passed in method call             | `5`, `10` in `sum(5, 10)`       |
| Formal Argument  | Parameter declared in method definition          | `int a`, `int b` in `sum(a, b)` |
| Method Signature | Method name + parameter types and order          | `sum(int, int)`                  |
---

### Rules to Follow in Method Call Statements

1. **Number of Arguments Must Match:**  
   The number of actual arguments in the method call must be the same as the number of formal parameters defined in the method.

2. **Type and Order Must Match:**  
   The data types and order of the actual arguments must exactly match the data types and order of the formal parameters in the method definition.

---

## 22. Method Overloading

**Method Overloading** means having multiple methods in the same class with the **same name** but **different parameter lists** (different number, type, or order of parameters).

Java uses method overloading to perform **compile-time polymorphism** (or static polymorphism).

---

### Key Points:

- Methods must have the **same name**.
- Parameter lists must differ in **number**, **type**, or **order**.
- Return type **can be same or different**, but it alone does **not** distinguish overloaded methods.
- Helps improve code readability by using the same method name for similar actions with different inputs.

---

### Example:

```java
public class Calculator {

    // Method to add two integers
    public int add(int a, int b) {
        return a + b;
    }

    // Overloaded method to add three integers
    public int add(int a, int b, int c) {
        return a + b + c;
    }

    // Overloaded method to add two double values
    public double add(double a, double b) {
        return a + b;
    }

    public static void main(String[] args) {
        Calculator calc = new Calculator();

        System.out.println(calc.add(5, 10));         // Calls add(int, int) → returns 15
        System.out.println(calc.add(5, 10, 15));     // Calls add(int, int, int) → returns 30
        System.out.println(calc.add(5.5, 10.5));     // Calls add(double, double) → returns 16.0
    }
}
```
---

## 23. Type Casting in Java

**Type casting** is the process of converting a variable from one data type to another.

---

### Two Types of Type Casting

1. **Primitive Type Casting** (between primitive data types)  
2. **Reference Type Casting** (between object types/classes)

---

## 1. Primitive Type Casting

### a) Widening Casting (Implicit)  
- Automatically done by Java.  
- Converts a smaller type to a larger type size.  
- No data loss.  

**Order:**  
`byte → short → int → long → float → double`

---

### **Example:**  
```java
int i = 100;
double d = i;  // int to double (widening), done automatically
```
---

b) Narrowing Casting (Explicit)
- Must be done manually by the programmer.
- Converts a larger type to a smaller type size.
- May cause data loss.

**Order:** 
`double → float → long → int → short → byte → char`

---

### **Example:**

```java
double d = 100.99;
int i = (int) d;  // double to int (narrowing), requires explicit cast
```
---

## 2. Reference Type Casting

### a) upcasting
### b) downcasting