# Android Interview Questions And Answers

# Kotlin

* **How do you declare variables in kotlin?**

```
val s: String = "Hi"
var x = 5
```

>var and val automatically detect the type using type inference.

* **What's the difference between val and car declaration? How to convert a String to an Int? val variables cannot be changed. They're like final.**

>Answer: var can be reassigned. But on next reassignment value should be of same data type.

>To convert string ot int use toInt() after string.

* **What's null safety and nullable types in kotlin? What is the elvis operator?**

>Kotlin puts a lot of weight behind null safety which is an approach to prevent the dreaded Null Pointer exception by using nullable types which are like String?.

* **What's a const? How does it differ from a val?**

>By default val properties are set at runtime. Adding a const modifier on a val would make a compile-time constant.

* **Does kotlin allow us to use primitive types such as int, float, double?**

>At the language level, we cannot use the above-mentioned types. But the JVM bytecode that's compiled does certainly have them.

* **How is !! differeent from ?.**

>!! is used to force unwrap the nullable type to ge the value. If the value returned is a null, it would lead to runtime crash.

* **What's the difference betweem == and === operators in kotlin?**

>== is used to compare the values are equal or not. === is used to check if the references are equal or not.

* **Access modifiers are same**

* **Extend class using : after class name**

* **By default classes are final in kotlin. To make them non-final use open modifier**

* **What are the types of constructors in kotlin?**

>Primary - Defined with class name with no logic handling
>Secondary - They are defined in the class body with logic handling.

* **What's init block in kotlin?**

init is the intialiser block in kotlin. It is executed once.

* **val are default type to define variable in constructor. But can be var**

* **Switch case is replaced with when**

```
when (num) {
	0..4 -> print("values is 0")
	5 -> print("value is 5")
	else -> print("default")
}
```

* **What are data class in kotlin?**

>In java you need to define toString(), hash() and copy() to use them. But in kotlin in these methods come by default in data class.

* **What is the difference between inline and infix functions?**

>Inline functions are used to save us memory overhead by preventing object allocations for the anonymous functions/lambda expressions called. Instead, it provides that functions body to the function that calls it at runtime. This increases the bytecode size slightly but saves a lot of memory.

>Infix functions on the other are used to call functions without parentheses or brackets. Doing so, the code looks much more like a natural language.

* **What's the difference between lazy and lateinit?**

lateinit means to initialize value later in code

lazy can be assigned to val but value in lazy is set at runtime

* **object can be used to create singleton class**

* **static variables and method can be defined using companion object**

* **Array can defined using arrayOf(1,2,3)**

* **Java vs kotlin**

1. kotlin removes boilerplate code
2. lambda expression just like java 1.8
3. 40% less coding

* **How do you declare a variable as volatile in kotlin?**

>By providing @volatile before variable declaration.

* **Ternary conditional operator can be defined using if condition**

* **There is dependency of secondary constructor on primary constructor.**

* **How do you think extension functions are useful?**

>Extension functions helps to extend a class with new functionality without having to inherit from class.

* **instanceof in kotlin works like object1 is object2**

* **way to define for loop in range**

```
for(i in 1..15){
}
```

* **kotlin doesn't support primitive datatype**

* **kotlin can be executed without JVM**

-----
#Data Structure

* **Array - ?**

* **Singly Linked List** - Each node in linked list contains data and a pointer. A pointer is a reference to the next item in the linked list. A linked list contains both a head and a tail.

https://github.com/sourabhrustagi/SinglyLinkedList

* **DoublyLinkedList** - A DoublyLinkedList is based on a linkedList, but there is two pointers in each node. Pointer is linked to previous and last. Last Node's next reference is null.

https://github.com/sourabhrustagi/DoublyLinkedList

* **Maps**

>A map represents a data structure in which collections of unique key and collections of values are stored where each key is associated with one value.

https://github.com/sourabhrustagi/maps

* **List**

* **Stack**

https://github.com/sourabhrustagi/Stack

* **Set**

* **HashSet**

* **Queue**

* **Sets**

* **Hash Tables**

* **Binary Tree** 

* **Binary Search tree**

* **Heap**

* **Hashing**

* **Graph**

* **Matrix**

* **Advanced Data Structure**

-----

# Android

* **Difference between activity and Fragment?**

An Activity is an component that provides a screen, with which users acn interact in order to do something. 

Whereas a Fragment represents a behaviour or a portion of user interface in an activity

* **Api call inspecting library**

>https://github.com/sourabhrustagi/StethoExample

* **Api call inspecting software**

>Charles Proxy

* **Moshi**

* **OkHttp**

* **Fast Networking Call**

* **Caching**

* **Glide**

* **Load image on scroll**

* **Dependency injection**

-----

# Java

* **What is difference between interfaces and abstract class?**

1. An Interface is a contract. 
2. An interface is an empty shell.
3. Interface only contains abstract methods.
4. Contains only final and static variables.
5. All methods should be public
6. Interface can extend mutiple interface

--

1. Abstract classes unlike interfaces are classes.
2. Abstract classes look a lot like interfaces.
