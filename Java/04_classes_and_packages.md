## 24. static

The `static` keyword in Java is used for memory management. It can be applied to variables, methods, blocks, and nested classes. When a member is declared `static`, it belongs to the **class** rather than instances of the class.

---

## 1. Static Variables

A static variable is shared among all instances of a class.

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

Static methods belong to the class rather than any object of the class. They can be called without creating an object.

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

Used to initialize static data. Executes only once when the class is loaded.

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

## 26. Constructor

## 27. Package