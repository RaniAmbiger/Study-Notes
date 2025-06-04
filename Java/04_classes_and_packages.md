## 24. static

The `static` keyword in Java is used for memory management. It can be applied to variables, methods, blocks, and nested classes. When a member is declared `static`, it belongs to the **class** rather than instances of the class.

---

## 1. Static Variables

- Declared using the static keyword.
- Only one copy exists for all instances.
- Useful for constants or counters..

### Exapmle

```java
class Example {
    static int count = 0;

    Example() {
        count++;
        System.out.println(count);//All objects share the same count variable.
    }
}
//Output:
//1
//2
//3
```
---

## 2. Static Methods

- Static methods belong to the class rather than any object of the class.
- Can be called without creating an object.
- Can only access static members directly.
- Cannot use this keyword.

### Exapmle

```java
class Example {
    static void display() {
        System.out.println("Static method called");
    }

    public static void main(String[] args) {
        Example.display();
    }
}
```
Rules:
- Can access only static data directly.
- Cannot use this or super keywords.

---

## 3. Static Blocks

- Used to initialize static data. 
- Executes only once when the class is loaded.

```java
class Example {
    static int num;

    static {
        num = 10;
        System.out.println("Static block executed");
    }

    public static void main(String[] args) {
        System.out.println("Main method");
    }
}
//Output:
//Static block executed
//Main method
```
---

## 4. Static Class (Nested Static Class)

A static class is a nested class that is a static member of its outer class.

```java
class Outer {
    static class Inner {
        void msg() {
            System.out.println("Hello from static nested class");
        }
    }
}

public class Test {
    public static void main(String[] args) {
        Outer.Inner obj = new Outer.Inner();
        obj.msg();
    }
}
//Output:
//Hello from static nested class
```
- Outer.Inner is a static nested class, so it can be accessed without creating an instance of Outer.
- We directly create an instance of Inner using Outer.Inner obj = new Outer.Inner();.

---


## 25. non-static

In Java, the non-static keyword is not explicitly used but refers to members (variables, methods, blocks) that belong to instances of a class (i.e., objects). Each object has its own separate copy of non-static members.

---

## 1. Non-Static Variables

- Declared without the static keyword.
- Each object of the class has its own copy.
- Cannot be accessed directly from a static context (like main() method) without creating an object.

### Example:
```java
public class Person {
    String name;  // non-static variable

    public static void main(String[] args) {
        Person p1 = new Person();
        Person p2 = new Person();

        p1.name = "Rani";
        p2.name = "Asha";

        System.out.println(p1.name); // Rani
        System.out.println(p2.name); // Asha
    }
}
```

---

## 2. Non-Static Methods

- Do not have the static keyword.
- Can access non-static variables directly.
- Must be called using an object of the class.

### Example:

```java
public class Calculator {
    int number;  // non-static variable

    // non-static method
    void setNumber(int n) {
        number = n;
    }

    void display() {
        System.out.println("Number is: " + number);
    }

    public static void main(String[] args) {
        Calculator calc = new Calculator();
        calc.setNumber(10);
        calc.display(); // Number is: 10
    }
}
```

---

## 3. Non-Static Block

- A block without static keyword.
- Runs each time an object is created.
- Used for instance-level initialization.

### Example:

```java
public class Example {
    // non-static block
    {
        System.out.println("This is a non-static block.");
    }

    Example() {
        System.out.println("Constructor called.");
    }

    public static void main(String[] args) {
        Example obj1 = new Example();
        Example obj2 = new Example();
    }
}
//Output:
// This is a non-static block.
// Constructor called.
// This is a non-static block.
// Constructor called.
```

## 26. Constructor

## 27. Package