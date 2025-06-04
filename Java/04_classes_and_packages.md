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

A constructor is a special method in Java that is called automatically when an object is created. It is used to initialize the object.

- Constructor name must be same as the class name.
- It does not have a return type, not even void.
- It is invoked automatically when an object is created.
- Used to set default or initial values to object properties.

### Example:

```java
public class Car {
    String model;

    // Constructor
    Car() {
        model = "Maruti";
        System.out.println("Constructor called");
    }

    public static void main(String[] args) {
        Car c = new Car();  // Constructor is automatically called
        System.out.println("Model: " + c.model);
    }
}
```
---

### Note

1️⃣	If no constructor is defined, Java provides a default constructor.
2️⃣	Constructors can be overloaded (i.e., multiple constructors with different parameters).
3️⃣	Constructors can call other constructors using this() and super().
4️⃣	Constructors cannot be inherited but can be called via super() in derived classes.

---

## Constructor Overloading

Defining multiple constructors in the same class with different parameter lists.

### Example:

```java
public class Student {
    String name;
    int age;

    Student() {
        name = "Unknown";
        age = 0;
    }

    Student(String n, int a) {
        name = n;
        age = a;
    }

    void display() {
        System.out.println(name + " - " + age);
    }

    public static void main(String[] args) {
        Student s1 = new Student();
        Student s2 = new Student("Rani", 22);
        s1.display(); // Unknown - 0
        s2.display(); // Rani - 22
    }
}
```
---

## Constructor Propagation

Constructor propagation occurs when a child class constructor automatically or explicitly calls the constructor of its parent class using super().
This ensures that the parent class is properly initialized before the child class.

### Example of Constructor Propagation
```java
class Animal {
    Animal() {
        System.out.println("Animal constructor called");
    }
}

class Dog extends Animal {
    Dog() {
        super();  // explicitly calling parent class constructor
        System.out.println("Dog constructor called");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();  // Constructor propagation starts here
    }
}
// Output:
// Animal constructor called
// Dog constructor called
```
---

### How It Works:

When Dog d = new Dog(); is executed, the Dog() constructor is called.

Inside Dog(), super(); is invoked (even if not written explicitly, Java calls it by default).

This causes the parent class constructor (Animal()) to execute first.

Once the parent constructor completes, the child constructor continues.

---

### Implicit Constructor Propagation

Even without writing super() explicitly, Java calls it automatically if there's a default constructor in the parent.

```java
class A {
    A() {
        System.out.println("A constructor");
    }
}

class B extends A {
    B() {
        // super() is automatically inserted by Java
        System.out.println("B constructor");
    }
}

public class Test {
    public static void main(String[] args) {
        B obj = new B();
    }
}
//Output:
// A constructor
// B constructor
```

---

## this, this(), super(), and Constructor Chaining

### this

* Refers to the current object.
* Used to resolve variable name conflicts.

```java
public class Demo {
    int a;

    Demo(int a) {
        this.a = a;  // 'this' refers to the instance variable
    }
}
```
---

### this()

* Calls another constructor in the same class.
* Must be the first statement in the constructor.

```java
class Sample {
    Sample() {
        this(10);
        System.out.println("Default constructor");
    }

    Sample(int x) {
        System.out.println("Parameterized constructor: " + x);
    }
}
```
---

### super()

* Calls a constructor from the parent class.
* Also must be the first statement in the constructor.

```java
class Animal {
    Animal() {
        System.out.println("Animal constructor");
    }
}

class Dog extends Animal {
    Dog() {
        super(); // calls Animal()
        System.out.println("Dog constructor");
    }
}
```
---

### Constructor Chaining

When one constructor calls another constructor in the same class or from parent class.

### Example (Constructor Chaining with this()):

```java
public class Book {
    String title;
    int price;

    Book() {
        this("Java Book", 500); // calls another constructor
    }

    Book(String t, int p) {
        title = t;
        price = p;
    }

    void show() {
        System.out.println(title + " - " + price);
    }

    public static void main(String[] args) {
        Book b = new Book(); // Constructor chaining in action
        b.show();
    }
}
```

## Package