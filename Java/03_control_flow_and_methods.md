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