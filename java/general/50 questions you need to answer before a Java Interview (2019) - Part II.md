---
created: 2023-05-25T23:38:14 (UTC +02:00)
tags: []
source: https://supernovaic.blogspot.com/2019/02/50-questions-you-need-to-answer-before_11.html
author: Edgar Regalado
---

# 50 questions you need to answer before a Java Interview (2019) - Part II

> ## Excerpt
> Photo by Helloquence  on Unsplash   Now it's time to continue with our preparation for our Java Interview!  Do you think you know it a...

---
[![](https://2.bp.blogspot.com/-oIwdUoW8c2Q/XFSIDPvRj_I/AAAAAAAAAk8/uC4Lc2qwCucU8OmhyA1cK1tM9tTpULRkwCLcBGAs/s400/interview-2.jpg)](https://2.bp.blogspot.com/-oIwdUoW8c2Q/XFSIDPvRj_I/AAAAAAAAAk8/uC4Lc2qwCucU8OmhyA1cK1tM9tTpULRkwCLcBGAs/s1600/interview-2.jpg)

Photo by [Helloquence](https://unsplash.com/photos/5fNmWej4tAA?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/search/photos/interview?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)  

  
Now it's time to continue with our [preparation for our Java Interview!](http://supernovaic.blogspot.com/2019/02/50-questions-you-need-to-answer-before.html) Do you think you know it all already? Alright! Let's test those skills!  

___

## **26.**    What is the method hashCode()? What is it used for?

The hashCode() method (_in a string_) is a complex calculation of the sort:  
  
s\[0\]\*31^(n - 1) + s\[1\]\*31^(n - 2) + ... + s\[n - 1\]  
  
Using int arithmetic, where s\[i\] is the ith character of the string, n is the length of the string, and ^ indicates exponentiation. (The hash value of the empty string is zero.)  
The method hashCode() _in an object_ returns the object’s memory address in hex. By definition, if two objects are equal, their hash code must also be equal.  
**Source: [Oracle](https://docs.oracle.com/javase/tutorial/java/IandI/objectclass.html)**

Hashcode is used for _bucket hashing_ that is for storing objects in a Hashmap. Hashmaps are usually divided into buckets and each bucket can contain several key/value pairs. The object's hashCode() determines which bucket it goes into, via this expression: object.hashCode() % n, where n = the total number of buckets and % is the modulus operator.  
  
Most often the objects will be well distributed across buckets, but you have no guarantee where they go. This depends on the data and the hashCode function.  
**Source: [Stackoverflow](https://stackoverflow.com/questions/18636576/what-is-meant-by-number-of-buckets-in-the-hashmap)**  
  
If you perform a contains() request, the hashmap will take the hashcode of the element, then look for the bucket where the hash code points to. If there’s more than one element in the bucket, the hashmap will use the method equals() to evaluate is the objects are equal.  
**Source: [Stackoverflow](https://stackoverflow.com/questions/3563847/what-is-the-use-of-hashcode-in-java)**  

## **27.**    What is the use of the equals() method?

The equals method allows us to evaluate if two objects are equal. The method has four characteristics: reflexive, symmetric, transitive, consistent. The equals method for class Object implements the most discriminating possible equivalence relation on objects; that is, for any non-null reference values x and y, this method returns true if and only if x and y refer to the same object (x == y has the value true).  
**Source: [Oracle](https://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#equals(java.lang.Object))**  

## **28.**    What is the relationship between equals() and hashCode()?

Whenever the method equals is overridden, the method hashcode() needs to be overridden as well, so as to maintain the general contract for the hashCode() method, which states that equal objects must have equal hash codes.  
**Source: [Oracle](https://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#equals(java.lang.Object))**

## **29.**    What are the main elements contained in the Collections Library?

Maps, Sets, and Lists. The three of them are interfaces that can be implemented differently through several implementers also contained in the library.  

## **30.**    What is the difference between a List, a Set, and a Map?

**List:** Represents an ordered sequence of objects. Each element has an index and they can be accessed, iterated, and removed according to the order in which they appear. Lists provide an ordered and indexed collection that **may contain duplicates**.  
  
**Set:** it is an unordered collection of unique objects. **Sets do not allow duplicates.** Certain implementations maintain the order.  
  
**Map:** A map is an ordered sequence of objects that consists of a **key, value pairs**. May contain duplicate values.  

## **31.**    What is the difference between ArrayList and LinkedList?

Both are implementations of the interface List. The difference is the element they use for storing the elements. ArrayList uses -as expected- a dynamic array to store the elements. LinkedLists use a doubly-linked list. ArrayList suits are better for storing and accessing data while LL is better for manipulating data (they are faster when removing because no bit shifting is required).  
  
**Source: [Javatpoint](https://www.javatpoint.com/difference-between-arraylist-and-linkedlist)**  
  

## **32.**    What are Maps?

Maps is an interface available in the Java Collections Library, which contains a collection of key, value pairs.  

## **33.**    Is a Map a class or an interface?

The Java Map is an interface that represents a mapping between a key and a value. Implementations of the Map include:

-     java.util.HashMap
-    java.util.Hashtable
-   java.util.EnumMap
-   java.util.IdentityHashMap
-   java.util.LinkedHashMap
-   java.util.Properties
-   java.util.TreeMap
-   java.util.WeakHashMap

## **34.**    Can you mention some typical uses of lists, sets, and maps?

The use of each collection depends on what we’re trying to achieve. For instance, if we want to identify elements based on an index, we should use a list. If we have to make sure that there are no duplicates, we should use a set. Last, Maps are used for key, value pair such as countries and currencies, language labels and definitions, etc.

## **35.** What is the keyword _final_ used for?

The keyword _final_ is used to indicate that specific elements won’t suffer further changes. It can be applied to a variable, a method, or a class. In each instance, it indicates something a little bit different, as follows:

-   _Final variable_: The value of the variable won’t change. In other words, it is a constant.
-   _Final Method_: The method cannot be overridden.
-   _Final Class_: The class cannot become a super-class. It stops inheritance.

**Source: [Javatpoint](https://www.javatpoint.com/final-keyword)**  

## **36.** What is it an exception?

An exception (or exceptional event) is a problem that arises during the execution of a program. When an Exception occurs the normal flow of the program is disrupted and the program/Application terminates abnormally, which is not recommended, therefore, these exceptions are to be handled.  
  
There are 3 classes of exceptions:

-   _Checked Exceptions: This is_ checked by the compiler at compilation time.
-   _Unchecked exceptions:_ Exception that occurs at the time of execution. They are also called: Runtime exceptions. They include bugs logic errors, improper use of API, among others.
-    _Errors._ These are not exceptions at all, but problems that arise beyond the control of the user or the programmer. Errors are typically ignored in your code because you can rarely do anything about an error. For example, if a stack overflow occurs, an error will arise. They are also ignored at the time of compilation.

**Source: [Tutorialspoint](https://www.tutorialspoint.com/java/java_exceptions.htm)**  

## **37.** What is the difference between an exception and a Runtime Exception?

This is connected to the type of exceptions: Exceptions are checked whereas Runtime exceptions are unchecked. Checked exceptions require that you handle the exception in a catch or declare the method as throwing the exception.  
_RuntimeExceptions_ are a subclass of Exception. Generally RuntimeExceptions are exceptions that can be prevented programmatically. E.g: NullPointerException. It is not necessary to catch these exceptions.  
  
**Source: [Stackoverflow](https://stackoverflow.com/questions/2190161/difference-between-java-lang-runtimeexception-and-java-lang-exception)**

## **38.** Do you need to catch a RuntimeException?

No. There’s no need to catch a Runtime Exception, but as a general good practice, it is recommended to do something about this exception. The best practice would be to identify the source of the Runtime Exception and fix the problem.  

## **39.** Do you need to add a throws in the method when creating a runtimeexception?

No. RunTimeExceptions belong to the family of unchecked exceptions which means that they do not need to be handled. Thus, there’s no need for a try/catch, nor for a throws declaration.  

## **40.** What is it an Error in Java?

An Error is a specific kind of Throwable, just as Exception is. The class Error is used to represent problems that are outside the control of the usual application: JVM errors, out of memory, problems verifying bytecode: these are things that you should not handle because if they occur, things are already so bad that your code is unlikely to be able to handle it sanely.  

## **41.** What are Generics in Java?

Generics in Java allows us to create non-specific type methods and classes. Therefore, the same method can be used for several data types. In the same manner, the same class can contain different data types.  
  
_Generic Methods_ are methods that can be called with arguments of different types. Based on the types of arguments passed to the generic method, the compiler handles each method call appropriately. Example:   
  
public class GenericMethodTest {  
   // generic method printArray  
   public static < E \> void printArray( E\[\] inputArray ) {  
      // Display array elements  
      for(E element : inputArray) {  
         System.out.printf("%s ", element);  
      }  
      System.out.println();  
   }  

   public static void main(String args\[\]) {  
      // Create arrays of Integer, Double and Character  
      Integer\[\] intArray \= { 1, 2, 3, 4, 5 };  
      Double\[\] doubleArray \= { 1.1, 2.2, 3.3, 4.4 };  
      Character\[\] charArray \= { 'H', 'E', 'L', 'L', 'O' };  
      System.out.println("Array integerArray contains:");  
      printArray(intArray);   // pass an Integer array  
      System.out.println("\\nArray doubleArray contains:");  
      printArray(doubleArray);   // pass a Double array  
      System.out.println("\\nArray characterArray contains:");  
      printArray(charArray);   // pass a Character array  

   }

  
_Generic Classes_ look like non-generic classes, but the class name is followed by a type parameter section. Example:  

public class Box<T\> {

   private T t;

   public void add(T t) {

      this.t \= t;  
   }  

   public T get() {

      return t;  
   }  

   public static void main(String\[\] args) {

      Box<Integer\> integerBox \= new Box<Integer\>();  
      Box<String\> stringBox \= new Box<String\>();

      integerBox.add(new Integer(10));

      stringBox.add(new String("Hello World"));  

      System.out.printf("Integer Value :%d\\n\\n", integerBox.get());

      System.out.printf("String Value :%s\\n", stringBox.get());  
   }  
}  
**Source: [Tutorialspoint](https://www.tutorialspoint.com/java/java_generics.htm)**  

## **42.** What is the StackOverflow? When is it produced?

  
Stackoverflow is an error produced when the program’s stack has run out of memory. The program stack stores the logical address of each function called. Therefore, if a function calls a huge amount of functions (like an infinite loop or a recursive function), the stack will run out of resources throwing the StackOverflowError.  
  
The common cause for a stack overflow is a bad recursive call. Typically, this is caused when your recursive functions don't have the correct termination condition, so it ends up calling itself forever.  
**Source: [Stackoverflow](https://stackoverflow.com/questions/214741/what-is-a-stackoverflowerror)**  

## **43.** What is a recursive function?

A recursive function is a function that calls itself. A typical use of recursive functions is to calculate the factorial of a number, the towers of Hanoi, the greatest common divisor, binary search, among others.  

## **44.** Besides stack, what are the other segments of the memory in JVM?

When a JVM executes a Java compiled program, during runtime it has 5 Memory segments:  
  
_Program Counter (PC) Register._ This segment stores the memory address of the Java Virtual Machine (JVM) instructions are currently being executed. A program counter is created every time a new thread is created. The program counter keeps a pointer to the current statements that are being executed in the current thread.  

_Method area_: Is used for storing various information about the program being executed. Information includes: Type Information (whether it is a class or an interface, type’s modifiers, Superclass, fully qualified name), a constant pool (for storing literals), Field information (Name, type, modifiers) and Method Information (Name, Return type, #, type and order of params, modifiers).

  
_Java Stack:_ Stores thread-specific data. Local variables, object references to a heap, etc. Whenever a thread enters a new method, a new block called a stack frame will be created inside stack memory for storing the method-specific details. When the thread completes the execution of that method, the corresponding stack frame will be pushed out of the stack memory.  
  
_Java Heap:_ Is the primary storage inside JVM and saves all new objects created during runtime. Heap mem is common for all threads and has two logical portions: Young and Old Generation. Young Generation stores the newly created objects. After some time, these objects get pushed into the old generation portion. f the total allocated memory is not sufficient for storing the new objects, then JVM will throw a java.lang.OutOfMemoryError.

[![](https://javabeat.net/wp-content/uploads/2016/02/jvm-memory-allocation.png)](https://javabeat.net/wp-content/uploads/2016/02/jvm-memory-allocation.png)

[**Source:**](https://www.blogger.com/blogger.g?blogID=8783164366670118553)  _Native Method Stack._ Similar to the Java Stack, stores the thread data for native method calls.  
  
[](https://www.blogger.com/blogger.g?blogID=8783164366670118553)[](https://www.blogger.com/blogger.g?blogID=8783164366670118553)[](https://www.blogger.com/blogger.g?blogID=8783164366670118553)[  
](https://www.blogger.com/blogger.g?blogID=8783164366670118553)**Source: [Javabeat](https://javabeat.net/jvm-memory/)**

## **45.** What does the Garbage Collector do?

The garbage collector is a program that runs on the Java Virtual Machine gets rid of objects which are not being used by a Java application anymore. It is a form of automatic memory management.  
  
When a typical Java application is running, it is creating new objects, but after a certain time, those objects are not used anymore. The garbage collector will look for those objects and get rid of them, freeing up the memory so other new objects can use that piece of memory.  
  
**Source:** [Stackoverflow](https://stackoverflow.com/questions/3798424/what-is-the-garbage-collector-in-java)

## **46.** What are the _threads_? What are they used for?

A thread is a thread of execution in a program. The Java Virtual Machine allows an application to have multiple threads of execution running concurrently.

Threads are used in concurrent programming to have multiple lines of execution and multiples parts of the code executing simultaneously, depending on the capabilities of the machine.  
  
**Source: [Oracle](https://docs.oracle.com/javase/7/docs/api/java/lang/Thread.html)**  

## **47.** What is the use of the keyword _synchronized_ in Java?

The Java synchronized keyword is an essential tool in concurrent programming in Java. Its overall purpose is to only allow one thread at a time into a particular section of code thus allowing us to protect, for example, variables or data from being corrupted by simultaneous modifications from different threads.  
  
At its simplest level, a block of code that is marked as synchronized in Java tells the JVM: "only let one thread in here at a time".  
  
**Source: [Javamex](https://www.javamex.com/tutorials/synchronization_concurrency_synchronized1.shtml)**

## **48.** What are the two types of synchronization supported in Java?

The Java programming language provides two basic synchronization idioms: _synchronized methods_ and _synchronized statements_.  
  
_Synchronized methods_ are declared by adding the _synchronized_ keyword in the declaration of the method. Making a method synchronized has two effects:

-   First, it is not possible for two invocations of synchronized methods on the same object to interleave. When one thread is executing a synchronized method for an object, all other threads that invoke synchronized methods for the same object block (suspend execution) until the first thread is done with the object.
-   Second, when a synchronized method exits, it automatically establishes a happens-before relationship with any subsequent invocation of a synchronized method for the same object. This guarantees that changes to the state of the object are visible to all threads.

  
_Synchronized statements_ are another way to introduce concurrent programming in Java. Unlike synchronized methods, synchronized statements must specify the object that provides the intrinsic lock.  
  
**Source: [Oracle](https://docs.oracle.com/javase/tutorial/essential/concurrency/locksync.html)**  
  

## DATABASE RELATED QUESTIONS

## 49\. What is a transaction in a DB?

Transactions are a group of one or more DB operations that form a single logical unit (serve a specific purpose).  
  
We’ll find the case where a logical operation cannot be achieved with a single Database statement (for several reasons, namely: several tables need to be updated, calculations have to be performed, etc). But what happens if one of the operations fails? If we persist with the changes, that will lead us to an inconsistent state in the Database.  
  
Transactions allow us to group all of these operations into a single logical unit that performs all of the operations and commits the result only after the last operation has been executed, thereby maintaining the consistency in the Database.  
  
If an error occurs, the DB allows performing a _rollback_, which returns the DB to the initial state, before the transaction, started its execution.  
  
For example, suppose that we have a supermarket. We have the entity product which is a catalog of the products available. This entity contains the attribute in\_stock which is the number of items we have in stock.  
  
Whenever we sell one exemplar of this product, we store the amount we sold in another entity (let’s call it SALE\_DETAIL) and we have to subtract the amount sold from the attribute in\_stock. Therefore, our transaction consists of two operations:

1.  Storing the amount sold in the entity SALE\_DETAIL.
    
2.  Subtracting the amount sold from the attribute in\_stock.

  
**Source: [Oracle](https://docs.oracle.com/database/121/CNCPT/transact.htm#CNCPT016)**  

## **50.** What are indexes in a DB? What are they used for? When should they be created?

Indexes in a DB are created in order to improve the efficiency of searches. They allow faster retrieval of records in a DB.  
  
Indexes should be created whenever we know that searches will be performed on a specific field. If we know that the user will be performing searches based on a specific field, we should create an index on that field to speed up the retrieval of information.  
  
**Source: [Techonthenet](https://www.techonthenet.com/oracle/indexes.php)**  
  
\[EXTRA QUESTION\]

## **51.** What type of indexes exists in Oracle?

  
The indexes can be categorized as follows:  
  
_B-tree indexes:_ These indexes are the standard index type. They are excellent for the primary key and highly selective indexes. Used as concatenated indexes, B-tree indexes can retrieve data sorted by the indexed columns. B-tree indexes have the following subtypes:  
  
_Index-organized tables:_ An index-organized table differs from a heap-organized because the data is itself the index.  
  
_Reverse key indexes:_ In this type of index, the bytes of the index key are reversed, for example, 103 is stored as 301. The reversal of bytes spreads out inserts into the index over many blocks.  
  
_Descending indexes:_ This type of index stores data on a particular column or columns in descending order.  
  
_B-tree cluster indexes:_ This type of index is used to index a table cluster key. Instead of pointing to a row, the key points to the block that contains rows related to the cluster key.  
  
_Bitmap and bitmap join indexes:_ In a bitmap index, an index entry uses a bitmap to point to multiple rows. In contrast, a B-tree index entry points to a single row. A bitmap join index is a bitmap index for the join of two or more tables.  
  
_Function-based indexes:_ This type of index includes columns that are either transformed by a function, such as the UPPER function, or included in an expression. B-tree or bitmap indexes can be function-based.  
  
_Application domain indexes:_ This type of index is created by a user for data in an application-specific domain. The physical index need not use a traditional index structure and can be stored either in the Oracle database as tables or externally as a file.  

**Source_:_ [Oracle](https://docs.oracle.com/cd/E11882_01/server.112/e40540/indexiot.htm#CNCPT1170)**  

And that's it, my fellow developers! I hope this summary of questions helps you land your dream job this 2019.  
All the best!
