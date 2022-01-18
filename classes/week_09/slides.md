# Java Programming Foundations 1

### Week 9: Objects and classes

---

## Overview

<span class="centered narrow">

- Objects
- Classes
- Syntax
- Abstractions
- Encapsulation
- The `File` class
- Imports
- Types

</span>

---

<!-- paginate: true -->

# Objects

---

## What are objects?

<p class="text narrower">Objects are a representation or an <span class="underline">abstraction</span> of an entity such as a car or a person.</p>

---

# Classes

---

## What are classes?

<p class="text narrower">Classes allow you to define data (attributes) and actions (methods) that relate to an entity.</p>

---

# How do classes relate to objects?

---

## How do classes relate to objects?

<p class="text narrow">Objects are created using classes.</p>

---

## How do classes relate to objects?

<p class="text narrow">Objects are the <span class="underline">instantiation</span> of a class.</p>

---

## How do classes relate to objects?

<p class="text narrow">Classes are the blueprints for objects.</p>

---

# You're already working with classes

---

## You're already working with classes

<p class="text narrow">Every time you create a new file in BlueJ, that's a class.</p>

---

## You're already working with classes

<p class="text narrow">Java comes with can use built-in classes.</p>

---

## You're already working with classes

<span class="centered narrow">

- `Math`
- `Scanner`
- `String`
- `System`

</span>

---

# Syntax

---

## Syntax

```java
// Modifiers
//  |
//  |  The word "class"
//  |   |
//  |   |    Name of the class
//  |   |      |
//  |   |      |
//  V   V      V
public class Calculator
{
// <------------------------+
//                          |
//                          |
//                          +---- Class body
//                          |
//                          |
// <------------------------+
}
```

---

## Sample of a class

```java
public class Calculator
{
    public static double add(double a, double b)
    {
        return a + b;
    }

    public static double subtract(double a, double b)
    {
        return a - b;
    }

    public static double multiply(double a, double b)
    {
        return a * b;
    }

    public static double divide(double a, double b)
    {
        return a / b;
    }
}
```

---

# Abstractions

---

## What is an abstraction?

<p class="text narrow">An abstraction is the representation of an idea.</p>

---

## Let's define a sample class for a car

![width:700px](assets/car.jpeg)

---

## Let's define a sample class for a car

<div class="centered narrow">

- What are the attributes a car has?
- What are the actions that a car can perform?

</div>

---

## What are the attributes of a car?

<div class="centered narrow">

- Exterior color
- Interior color
- Number of doors
- Number of wheels
- Maximum number of passengers

</div>

---

## What are the actions a car can perform?

<div class="centered narrow">

- Drive forward
- Drive backward
- Turn left
- Turn right
- Break

</div>

---

# Let's write some code

---

## The `Car` class

```java
public class Car
{
    public static void driveForward()
    {
        System.out.println("Driving forwards");
    }

    public static void driveBackward()
    {
        System.out.println("Driving backwards");
    }

    public static void turnLeft()
    {
        System.out.println("Turning left");
    }

    public static void turnRight()
    {
        System.out.println("Turning right");
    }

    public static void stop()
    {
        System.out.println("Stopping");
    }
}
```

---

## The `Runner` class

```java
public class Runner
{
    public static void main(String[] args) throws IOException
    {
        Car.driveForward();
        Car.turnLeft();
        Car.turnRight();
        Car.stop();
    }
}
```

---

# Encapsulation

---

## What is encapsulation?

<p class="text narrower">Encapsulation is the packaging or grouping of logic and behaviour into a unit.</p>

---

## What is encapsulation?

<p class="text narrower">Encapsulation is the packaging or grouping of logic and behaviour into a <span class="underline">class</span>.</p>

---

## The packaging of behaviour into a class

<p class="text narrower">Car related code goes in the <code>Car</code> class.</p>

---

# The `File` class

---

## What can it do?

<p class="text narrow">Allows you to read and write to files in your computer.</p>

---

# Let's write some code

---

<p class="text narrow">Print the contents of a file using the <code>File</code> and <code>Scanner</code> classes.</span>

---

```java
import java.io.*;
import java.util.*;

public class PrintFile
{
    public static void main(String[] args) throws IOException
    {
        System.out.print("Path to a file: ");
        Scanner userInput = new Scanner(System.in);
        String inputFilePath = userInput.nextLine();

        File inputFile = new File(inputFilePath);
        Scanner inputFileScanner = new Scanner(inputFile);

        while (inputFileScanner.hasNext()) {
            String line = inputFileScanner.nextLine();
            System.out.println(line);
        }
    }
}
```

---

## Objects are the instantiation of a class

<p class="text narrow">Instantiation is to create a "copy" of something.</p>

---

## Objects are the instantiation of a class

<p class="text narrow">Use the <code>new</code> keyword to instantiate a class.</p>

---

## Objects are the instantiation of a class

```java
File inputFile = new File(inputFilePath);
Scanner inputFileScanner = new Scanner(inputFile);
```

---

# Imports

---

## Imports

<p class="text narrow">Use the <code>import</code> keyword to gain access to a class defined externally.</p>

---

## Imports

```
import java.io.*;
import java.util.*;
```

---

## Imports

<span class="centered wide">

- `import java.io.*` gives you access to `File` and `IOException`,
- `import java.util.*` gives you access to `Scanner`

</span>

---

# Types

---

## Types

<p class="text narrow">Every class is a type.</p>

---

## Every class is a type

```java
Scanner userInput = new Scanner(System.in);
String inputFilePath = userInput.nextLine();

File inputFile = new File(inputFilePath);
Scanner inputFileScanner = new Scanner(inputFile);
```
