---
created: 2023-05-25T23:37:26 (UTC +02:00)
tags: []
source: https://supernovaic.blogspot.com/2019/02/50-questions-you-need-to-answer-before.html
author: Edgar Regalado
---

# 50 Questions you need to answer before a Java Interview (2019) - Part 1

> ## Excerpt
> Photo by Johanna Buguet  on Unsplash  As the end of my studies is coming, I've endeavored in the laborious task of getting a job as...

---
[![](https://2.bp.blogspot.com/-lXeAq6FJKBQ/XFMQuPipO-I/AAAAAAAAAkw/HYSIYawUJEQMv4vf8R6goRrOymyeUr9DwCLcBGAs/s400/interview-1.jpg)](https://2.bp.blogspot.com/-lXeAq6FJKBQ/XFMQuPipO-I/AAAAAAAAAkw/HYSIYawUJEQMv4vf8R6goRrOymyeUr9DwCLcBGAs/s1600/interview-1.jpg)

Photo by [Johanna Buguet](https://unsplash.com/photos/u5L8EFY1RT4?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/search/photos/interview?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)**_<sub><sup><strike><br></strike></sup></sub>_**  
  
As the end of my studies is coming, I've endeavored in the laborious task of getting a job as a software developer. Having a lot of practical experience behind me, I thought it'd be an easy task. It has been proven, however, to be a more difficult task than I first thought.  
  
The reason for this was mainly due to my lack of theoretical knowledge. I was focusing too much on the practical side and forgot about the underlying theory. Therefore, in this article, I'll be sharing with you 50 real questions that I have been asked during interviews. Each question comes with an answer and some of them also have references to read more on the topic. Let's nail that job!  

___

## GENERAL KNOWLEDGE ABOUT PROGRAMMING

## **1.**    What is it a class? What is an object? What’s the difference between them?

_Class_: A class is an abstraction of real objects. A class is an archetype, a model, a blueprint that serves as the basis for constructing different objects and contains the definition of several attributes, methods, or actions that are common for every object.

_Object_: This is a specific instance of a class. It has specific values for every single attribute.

## 2.    What is encapsulation?

Encapsulation means that all of the values of the attributes of a specific object are wrapped within the object and thus not accessible to foreign objects. The objective is to make sure that “sensitive” data is hidden from users. This is achieved by declaring the attributes as private. To allow access, it is done through get/set methods.

Reasons:

-   Better control of class attributes and methods
    
-   Class variables can be made read-only (if you omit the set method), or write-only (if you omit the get method)
    
-   Flexible: the programmer can change one part of the code without affecting other parts
    
-   Increased security of data
    

**Source**: [W3schools](https://www.w3schools.com/java/java_encapsulation.asp)

## 3.    What is an abstract class?

An abstract class is a class that cannot be instantiated. It usually serves as a super-model for other classes that inherit its attributes and methods. It provides a common interface that allows subclasses to be interchanged with all other subclasses.  
  

## **4.**    What is it an immutable class?

An immutable class is a class whose instances cannot be modified. It is initialized at construction time and cannot be modified later on in the execution of the program.

They are efficient and secure, also thread-safe. They are especially useful in concurrent applications.  

## **5.**    What is it an interface?

An interface is a reference type in Java. It is a collection of abstract methods. It contains only the declaration of the methods, but its body is implemented elsewhere. Another class implements the interface, thereby inheriting the abstract methods. The implementer class contains the definition of the methods.

## **6.**    Can you create the body of a method in an interface?

Normally No. The body of the method should be created in the implementer class. However, this functionality has been added in Java 8 through the so-called Default Methods.

## **7.**    What are the default methods?

Default methods are methods whose implementation is present in the interfaces themselves. They are only available from Java 8 onwards. Therefore, an implementer does not need to override the methods from an interface (but it can do so).

## **8.**    What is method overriding? 

Method overriding is possible thanks to inheritance. When we have a super class with method A, every subclass inheriting from it can have different implementations of the method, according to the class needs. In simple words: Method overriding is present when a subclass provides the specific implementation of the method that has been declared by its parent class. Method overriding should meet three criteria:

-             The method should have the same name in the super and subclasses.
    
-             The method must have the same parameters as in the parent class.
    
-             The must be an IS-A relationship (inheritance).
    

Overriding is possible through the annotation: @Override  
**Source: [Oracle](https://docs.oracle.com/javase/tutorial/java/IandI/override.html)**  

## **9.**    Can you override the construct of a class?

No, constructors cannot be overridden.

## **10.**    Can you override static methods? 

No. When we create a static method in a subclass with the same name and parameters as in the upper class, the static method in the super class is hidden.   
**Source: [Oracle](https://docs.oracle.com/javase/tutorial/java/IandI/override.html)**  

## **11.**    What is a “default construct” of a class?

A default constructor is a constructor with no formal parameters and no throws clause, automatically generated by the compiler if no other constructor has been specified.   
**Source:** [Oracle](https://docs.oracle.com/javase/specs/jls/se7/html/jls-8.html#jls-8.8.9)

## **12.**    What does method overloading mean? 

Method overloading occurs when we have multiple methods having the same name, but different parameters. Overloading can occur by changing the number of arguments or the data type.  
**Source: [Javatpoint](https://www.javatpoint.com/method-overloading-in-java)**  

## **13.** In what consists of the design pattern, Singleton?

Singleton is a design pattern that assures that only a single instance of an object exists. It achieves so, by declaring a static object of itself within the class and making the constructor private. Therefore, the only way to access it is through the static object.  
  
The singleton pattern also belongs to the creational patterns and is based on the statement that the class contains a static instance of itself. This instance can be accessed through a static method called getInstance(). The constructor of this class should be private. Therefore, this class cannot be instantiated, assuring that there exists only a single object of this class at all times.  
**Source: [Tutorialspoint](https://www.tutorialspoint.com/design_pattern/singleton_pattern.htm)**

## **14.** What is the Factory Pattern?

The factory pattern is a design pattern in which, instead of using the habitual operator new to create objects, we create a specialized class that handles the creation of multiple objects. To create a new object, we make use of a Factory class which is in charge of setting the appropriate attributes and values.  
**Source: [Tutorialspoint](https://www.tutorialspoint.com/design_pattern/factory_pattern.htm)**  

## **15.** Is Multiple inheritances possible in Java?

Java does not allow to extend from more than one class to avoid issues of _multiple inheritances of state._   
However, Java allows _multiple inheritance of type_ which is the ability of a class to implement more than one interface.  
**Source: [Oracle](https://docs.oracle.com/javase/tutorial/java/IandI/multipleinheritance.html)**

## **16.** What is the composition in Java?

Composition defines an aggregation relationship on the sense that Class “A” has-a class “B”. An example can be the class CAR has a class Wheel. In this sense, one of the attributes of a class is another class. 

## **17.** What are the access modifiers in Java?

The access modifiers are a set of keywords that allow the modification of access levels for classes, variables, methods, and constructors. There are 4 access modifiers in Java:

-           _Default_: No access modifier is defined. Variables and methods become visible to the whole package.
    
-           _Private:_ Members are only visible within the same class.
    
-           _Protected:_ Variables and methods are visible within the class and any other subclass inheriting from it.
    
-           _Public:_ Public members are accessible everywhere.
    

**Source: [Tutorialspoint](https://www.tutorialspoint.com/java/java_access_modifiers.htm)**

## **18.** What is it an inner class?

An inner class -also called _nested class_\- is a class in which declaration forms part of the declaration of another class. Generally speaking, there are two types of nested classes: Static and non-static.  
Benefits of nested classes include: It allows the usage of access modifiers within the class, therefore making it possible to create private classes. Also, inner classes have access to the private variables of the outer class.  
**Source: [Tutorialspoint](https://www.tutorialspoint.com/java/java_innerclasses.htm)**

## **19.** What is it a local class?

A local class is a class defined in a block. For example, you can define a local class in a method body, a for loop, or an if clause.  
**Source: [Oracle](https://docs.oracle.com/javase/tutorial/java/javaOO/localclasses.html)**  

## **20.** What is it an anonymous class? When can we use it?

An anonymous class is a local class without a name. That is: a class that is defined in a block (a for, a method, an if) and has no name. We use them only if we need to use a local class only once.  
It is recommended to use anonymous classes when there’s a need to declare fields or additional methods.  
**Source: [Oracle-1](https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html)**  
[Oracle-2](https://docs.oracle.com/javase/tutorial/java/javaOO/whentouse.html)

## **21.** What is an expression, a statement, and a block?

An _expression_ is a construct made up of variables, operators, and method invocations, which are constructed according to the syntax of the language, that evaluates a single value. Example: _cadence = 0, 1\*2\*3, (x+y)/100._  
_Statements_ are roughly equivalent to sentences in natural languages. A statement forms a complete unit of execution. The following types of expressions can be made into a statement by terminating the expression with a semicolon (;). Example:

// assignment statement  
aValue = 8933.234;  
// increment statement

aValue++;  
// method invocation statement  
System.out.println("Hello World!");  
// object creation statement  
Bicycle myBike = new Bicycle();

A _block_ is a group of zero or more statements between balanced braces and can be used anywhere a single statement is allowed. The following example, BlockDemo, illustrates the use of blocks:

class BlockDemo {

     public static void main(String\[\] args) {  
          boolean condition = true;

          if (condition) { **// begin block 1**

               System.out.println("Condition is true.");

          } **// end block one**

          else { **// begin block 2**

               System.out.println("Condition is false.");

          } **// end block 2**

     }

}

**Source: [Oracle](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html)**  

## **22.** What is dependency injection?

Dependency injection is basically providing the objects that an object needs (its dependencies) instead of having it construct them itself. It's a very useful technique for testing since it allows dependencies to be mocked or stubbed out.  
Dependencies can be injected into objects by any means (such as constructor injection or setter injection). One can even use specialized dependency injection frameworks (e.g. Spring) to do that, but they certainly aren't required.

Example:

public SomeClass() {  
    myObject = Factory.getObject();  
}

  
Applying dependency injection to the previous code, you’ll have:

public SomeClass (MyClass myObject) {

    this.myObject = myObject;

}

  
Now, myObject is received as an argument, and SomeClass does not have to deal with its creation/initialization. Therefore, the dependency myObject is being injected in SomeClass.

## **23.** What is the spring framework?

The Spring Framework is an application framework for Java. Spring’s core features can be used by any Java app, but extensions allow the creation of web apps on top of Java EE. It is an open source.  
**Source:** [Wikipedia](https://en.wikipedia.org/wiki/Spring_Framework)

## **24.** What is the keyword transient used for?

Before understanding the transient keyword, one has to understand the concept of serialization.  
_Serialization_ is the process of making the object’s state persistent. That means the state of the object is converted into a stream of bytes and stored in a file. In the same way, we can use deserialization to bring back the object's state from bytes.  
The keyword _transient_ indicates that a variable is not part of the persistent state of an object. This means, the content of the variable should not be persisted into a file and should be derived programmatically from other fields. Consider the following example:

  

class GalleryImage implements Serializable

{

    private Image image;

    private transient Image thumbnailImage;

    private void generateThumbnail()  
    {  
        // Generate thumbnail.  
    }

    private void readObject(ObjectInputStream inputStream)

            throws IOException, ClassNotFoundException  
    {  
        inputStream.defaultReadObject();  
        generateThumbnail();  
    }     
}

In the example, the attribute image is serializable. That means, it forms part of the persistent state of the object. On the other hand, thumbnailImage is _transient_, therefore it won’t be persisted. This example would save storage capacity.  

## 25**.**    How can we compare two strings in Java?

String comparison in Java is a special topic. Instead of using the habitual operator ==, we should use the method _equals()_ to verify if the value of two strings is the same.

\== tests for reference equality (whether they are the same object).

.equals() tests for value equality (whether they are logically "equal").

// These two have the same value

new String("test").equals("test") // --> true

// ... but they are not the same object

new String("test") == "test" // --> false

// ... neither are these

new String("test") == new String("test") // --> false

// ... but these are because literals are interned by

// the compiler and thus refer to the same object  
"test" == "test" // --> true

// ... string literals are concatenated by the compiler

// and the results are interned.  
"test" == "te" + "st" // --> true

**Source****: [Stackoverflow](https://stackoverflow.com/questions/513832/how-do-i-compare-strings-in-java)**  
  
Stay tuned as we'll post [Part 2](http://supernovaic.blogspot.com/2019/02/50-questions-you-need-to-answer-before_11.html) next week! In the meantime, good luck with those job interviews!
