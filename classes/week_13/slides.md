# Java Programming Foundations 1

### Week 13: Review + Polymorphism

---

## Overview

<span class="centered narrow">

- Abstract classes review
- Inheritance review
- Polymorphism
- Practice time

</span>

---

<!-- paginate: true -->

# Abstract classes

---

## Abstract classes

<p class="text narrower">
An abstract class is just like a regular class but cannot be instantiated.
</p>

---

## Abstract classes

<p class="text narrower">
Abstract classed are meant to be inherited.
</p>

---

# Inheritance

---

## Inheritance

<p class="text narrower">
Classes are able to extend each other with inheritance.
</p>

---

## Inheritance

<p class="text narrower">
A "child" class inherits from a "parent" class.
</p>

---

## Inherited example

```java
public class Parent
{
    // ...
}

public class Child extends Parent
{
    // ...
}
```

---

## Inheritance

<p class="text narrower">
A "child" class inherits all behaviour from its "parent" class and can be used
in place of its parent.
</p>

---

## ... can be used in place of its parent.

<p class="text narrower">
This is a form of polymorphism. More on polymorphism in a minute.
</p>

---

## Abstract class inheritance example (1)

```java
public abstract class Pokemon
{
    protected String name;
    protected int attack;
    protected int health;

    public String getName() { return this.name; }
    public int getAttack() { return this.attack; }
    public int getHealth() { return this.health; }
}

public class Pikachu extends Pokemon
{
    public Pikachu()
    {
        this.name = "Pikachu";
        this.attack = 6;
        this.health = 110;
    }
}
```

---

## Abstract class inheritance example (2)

```java
public class App
{
    public static void main(String[] args)
    {
        Pokemon pokemon1 = new Pikachu();

        System.out.println(pokemon1.getName() + " has " +
            pokemon1.getHealth() + " health and " +
            pokemon1.getAttack() + " attack");
    }
}
```

---

# Polymorphism

---

## Polymorphism

<p class="text narrower">
There are different forms of polymorphism, but the one we will focus on is
polymorphism via inheritance.
</p>

---

## Polymorphism

<p class="text narrower">
Polymorphism allows you to work with objects of different types using a single
interface.
</p>

---

# Practice time
