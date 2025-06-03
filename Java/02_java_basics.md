## 🔢 11. Types of Data in Java

- **Numeric Data:** Integers and floating-point numbers (e.g., 10, 25.5)
- **Boolean Data:** Represents true or false values.
- **Character Data:** Single characters (e.g., 'A', 'z').
- **String Data:** Sequence of characters enclosed in double quotes (e.g., "Java").

---

## 🔢 12. Data Types in Java

Java supports **two types** of data types:

### 🔹 1. Primitive Data Types (8 types)

| Data Type | Size     | Default Value | Description                  |
|-----------|----------|---------------|------------------------------|
| byte      | 1 byte   | 0             | Small integer value          |
| short     | 2 bytes  | 0             | Short integer                |
| int       | 4 bytes  | 0             | Integer value                |
| long      | 8 bytes  | 0L            | Long integer value           |
| float     | 4 bytes  | 0.0f          | Decimal value (single-precision) |
| double    | 8 bytes  | 0.0d          | Decimal value (double-precision) |
| char      | 2 bytes  | '\u0000'     | Single character             |
| boolean   | 1 bit    | false         | true or false                |

> Note: `float` and `double` are used for decimal values; `float` requires `f` or `F` suffix.

### 🔹 2. Non-Primitive Data Types
- Also known as **reference types**.
- Examples: `String`, `Arrays`, `Classes`, `Interfaces`, `Objects`.

---

## 🧰 13. Variables in Java

- Variables are **containers to store data**.
- Must be declared before use.
- **Types of Variables:**
  - **Local Variable:** Declared inside a method, accessible only within the method.
  - **Static Variable:** Shared among all instances of a class (class-level variable).
  - **Non-Static Variable:** Instance variable unique to each object.

---

## 🔠 14. Tokens in Java

- The smallest unit in Java program.
- Types of tokens:
  - Keywords
  - Identifiers
  - Literals
  - Operators
  - Separators (like `;`, `{}`, `()`, etc.)

---

## 📚 15. Keywords in Java

- Reserved words with special meaning.
- Cannot be used as identifiers.
- Examples include `class`, `public`, `static`, `void`, `int`, `if`, `else`, `while`, etc.
- Java has **50+ keywords**.

---

## 🆔 16. Identifiers in Java

- Names used for variables, methods, classes, etc.
- **Rules for Identifiers:**
  1. Must begin with a letter (A-Z or a-z), underscore (_) or dollar sign ($).
  2. Subsequent characters can be letters, digits (0-9), underscores, or dollar signs.
  3. Cannot be a keyword.
  4. Case-sensitive (`myVar` and `MyVar` are different).
  5. No spaces allowed.
  6. Should be meaningful and descriptive.

---

## ⚙️ 17. Operators in Java

Operators are special symbols that perform operations on variables and values. Java supports various types of operators as described below:

---

## 1. Arithmetic Operators
Used to perform basic mathematical operations.

| Operator | Description        | Example   | Result  |
|----------|--------------------|-----------|---------|
| `+`      | Addition           | `5 + 3`   | 8       |
| `-`      | Subtraction        | `5 - 3`   | 2       |
| `*`      | Multiplication     | `5 * 3`   | 15      |
| `/`      | Division           | `15 / 3`  | 5       |
| `%`      | Modulus (remainder)| `5 % 3`   | 2       |

**Example:**
```java
int a = 10, b = 3;
System.out.println(a + b);  // Output: 13
System.out.println(a % b);  // Output: 1
```

## 2. Assignment Operators in Java

Assignment operators are used to assign values to variables. They not only assign but can also perform arithmetic operations and then assign the result to the variable.

---

### List of Assignment Operators

| Operator | Description                         | Example          | Equivalent To         |
|----------|-----------------------------------|------------------|----------------------|
| `=`      | Simple assignment                 | `a = 10`         | `a = 10`             |
| `+=`     | Add and assign                   | `a += 5`         | `a = a + 5`          |
| `-=`     | Subtract and assign              | `a -= 5`         | `a = a - 5`          |
| `*=`     | Multiply and assign              | `a *= 5`         | `a = a * 5`          |
| `/=`     | Divide and assign                | `a /= 5`         | `a = a / 5`          |
| `%=`     | Modulus and assign (remainder)  | `a %= 5`         | `a = a % 5`          |

---

### How it works

- The right-hand expression is evaluated first.
- The result is then assigned to the variable on the left-hand side.

---

### Examples

```java
int a = 10;

a += 5;    // Equivalent to a = a + 5;  a becomes 15
System.out.println(a);  // Output: 15

a -= 3;    // Equivalent to a = a - 3;  a becomes 12
System.out.println(a);  // Output: 12

a *= 2;    // Equivalent to a = a * 2;  a becomes 24
System.out.println(a);  // Output: 24

a /= 4;    // Equivalent to a = a / 4;  a becomes 6
System.out.println(a);  // Output: 6

a %= 4;    // Equivalent to a = a % 4;  a becomes 2
System.out.println(a);  // Output: 2
```

## 3. Relational Operators in Java

Relational operators are used to compare two values or expressions. They return a boolean value (`true` or `false`) based on the comparison result.

---

### List of Relational Operators

| Operator | Description                   | Example           | Result Type |
|----------|-------------------------------|-------------------|-------------|
| `==`     | Equal to                     | `a == b`          | boolean     |
| `!=`     | Not equal to                 | `a != b`          | boolean     |
| `>`      | Greater than                 | `a > b`           | boolean     |
| `<`      | Less than                    | `a < b`           | boolean     |
| `>=`     | Greater than or equal to     | `a >= b`          | boolean     |
| `<=`     | Less than or equal to        | `a <= b`          | boolean     |

---

### How it works

- These operators compare two values or variables.
- The result is always a boolean (`true` or `false`).
- Used frequently in decision-making statements like `if`, `while`, and `for`.

---

### Examples

```java
int a = 10;
int b = 20;

System.out.println(a == b);  // false, because 10 is not equal to 20
System.out.println(a != b);  // true, because 10 is not equal to 20
System.out.println(a > b);   // false, because 10 is not greater than 20
System.out.println(a < b);   // true, because 10 is less than 20
System.out.println(a >= 10); // true, because 10 is equal to 10
System.out.println(b <= 20); // true, because 20 is equal to 20
```

## 4. Increment Operators in Java

Increment operators are used to increase the value of a variable by 1. They are commonly used in loops and counters.

---

### Types of Increment Operators

| Operator | Description                      | Example        | Effect                          |
|----------|---------------------------------|----------------|--------------------------------|
| `++var`  | Pre-increment: increments first, then uses the value | `++a`          | Increments `a` by 1, then uses `a` |
| `var++`  | Post-increment: uses the value first, then increments | `a++`          | Uses `a`, then increments `a` by 1  |

---

### How it works

- **Pre-increment (`++var`)**: The variable is incremented by 1 **before** its value is used in the expression.
- **Post-increment (`var++`)**: The current value of the variable is used in the expression **before** it is incremented by 1.

---

### Examples

```java
int a = 5;

System.out.println(++a);  // Output: 6 (a is incremented before printing)
System.out.println(a);    // Output: 6

int b = 5;

System.out.println(b++);  // Output: 5 (b is printed before increment)
System.out.println(b);    // Output: 6
```

## 5. Decrement Operators in Java

Decrement operators are used to decrease the value of a variable by 1. They are often used in loops and counters.

---

### Types of Decrement Operators

| Operator | Description                      | Example        | Effect                          |
|----------|---------------------------------|----------------|--------------------------------|
| `--var`  | Pre-decrement: decrements first, then uses the value | `--a`          | Decrements `a` by 1, then uses `a` |
| `var--`  | Post-decrement: uses the value first, then decrements | `a--`          | Uses `a`, then decrements `a` by 1  |

---

### How it works

- **Pre-decrement (`--var`)**: The variable is decremented by 1 **before** its value is used in the expression.
- **Post-decrement (`var--`)**: The current value of the variable is used in the expression **before** it is decremented by 1.

---

### Examples

```java
int a = 5;

System.out.println(--a);  // Output: 4 (a is decremented before printing)
System.out.println(a);    // Output: 4

int b = 5;

System.out.println(b--);  // Output: 5 (b is printed before decrement)
System.out.println(b);    // Output: 4
```

## 6. Logical Operators in Java

Logical operators are used to combine multiple boolean expressions or conditions. They help in decision making by evaluating expressions to `true` or `false`.

---

### Types of Logical Operators

| Operator | Name           | Description                                  | Example                | Result Type |
|----------|----------------|----------------------------------------------|------------------------|-------------|
| `&&`     | Logical AND    | Returns `true` if **both** operands are true | `(a > 5) && (b < 10)`  | boolean     |
| `||`     | Logical OR     | Returns `true` if **at least one** operand is true | `(a > 5) || (b < 10)`  | boolean     |
| `!`      | Logical NOT    | Returns the **opposite** boolean value        | `!(a == b)`            | boolean     |

---

### How Logical Operators Work

- **AND (`&&`)**: Both conditions must be true for the whole expression to be true.
- **OR (`||`)**: At least one condition must be true for the whole expression to be true.
- **NOT (`!`)**: Inverts the boolean value; true becomes false, and false becomes true.

---

### Truth Tables

**AND (`&&`):**

| A     | B     | A && B |
|-------|-------|---------|
| true  | true  | true    |
| true  | false | false   |
| false | true  | false   |
| false | false | false   |

**OR (`||`):**

| A     | B     | A \|\| B |
|-------|-------|-----------|
| true  | true  | true      |
| true  | false | true      |
| false | true  | true      |
| false | false | false     |

**NOT (`!`):**

| A     | !A    |
|-------|-------|
| true  | false |
| false | true  |

---

### Examples

```java
boolean a = true;
boolean b = false;

System.out.println(a && b);  // false (both not true)
System.out.println(a || b);  // true  (one true)
System.out.println(!a);      // false (inverts true)
System.out.println(!b);      // true  (inverts false)

// Using logical operators in conditions
int x = 10;
int y = 20;

if (x > 5 && y < 25) {
    System.out.println("Both conditions are true");
}

if (x > 15 || y < 25) {
    System.out.println("At least one condition is true");
}
```

## Conditional (Ternary) Operator in Java

- The **conditional operator** (also called the ternary operator) is a shorthand for simple `if-else` statements. It evaluates a condition and returns one of two values depending on whether the condition is true or false.

---

### Syntax

```java
condition ? expression1 : expression2;
```
---

### Examples of Conditional (Ternary) Operator in Java

```java
// Example 1: Find the maximum of two numbers
int a = 10, b = 20;
int max = (a > b) ? a : b;
System.out.println("Max is " + max);  // Output: Max is 20

// Example 2: Check voting eligibility
int age = 18;
String eligibility = (age >= 18) ? "Eligible to vote" : "Not eligible to vote";
System.out.println(eligibility);  // Output: Eligible to vote

// Example 3: Nested ternary for grading
int marks = 75;
String grade = (marks >= 90) ? "A" :
               (marks >= 75) ? "B" :
               (marks >= 50) ? "C" : "F";
System.out.println("Grade: " + grade);  // Output: Grade: B
```