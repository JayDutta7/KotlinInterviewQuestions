# Kotlin Interview Questions And Answers

* How do you declare variables in kotlin?

```
val s: String = "Hi"
var x = 5
```

>var and val automatically detect the type using type inference.

* What's the difference between val and car declaration? How to convert a String to an Int? val variables cannot be changed. They're like final.

>Answer: var can be reassigned. But on next reassignment value should be of same data type.

>To convert string ot int use toInt() after string.

* What's null safety and nullable types in kotlin? What is the elvis operator?

>Kotlin puts a lot of weight behind null safety which is an approach to prevent the dreaded Null Pointer exception by using nullable types which are like String?.

* What's a const? How does it differ from a val?

>By default val properties are set at runtime. Adding a const modifier on a val would make a compile-time constant.

* Does kotlin allow us to use primitive types such as int, float, double?

>At the language level, we cannot use the above-mentioned types. But the JVM bytecode that's compiled does certainly have them.

* How is !! differeent from ?.

>!! is used to force unwrap the nullable type to ge the value. If the value returned is a null, it would lead to runtime crash.

* What's the difference betweem == and === operators in kotlin?

>== is used to compare the values are equal or not. === is used to check if the references are equal or not.

* access modifiers are same

* Extend class using : after class name

* By default classes are final in kotlin. To make them non-final use open modifier

* What are the types of constructors in kotlin?

>Primary - Defined with class name with no logic handling
>Secondary - They are defined in the class body with logic handling.

* What's init block in kotlin

init is the intialiser block in kotlin. It is executed once.

* val are default type to define variable in constructor. But can be var

* Switch case is replaced with when

```
when (num) {
	0..4 -> print("values is 0")
	5 -> print("value is 5")
	else -> print("default")
}
```

* What are data class in kotlin?

>In java you need to define toString(), hash() and copy() to use them. But in kotlin in these methods come by default in data class.

* What is the difference between inline and infix functions?

>Inline functions are used to save us memory overhead by preventing object allocations for the anonymous functions/lambda expressions called. Instead, it provides that functions body to the function that calls it at runtime. This increases the bytecode size slightly but saves a lot of memory.

>Infix functions on the other are used to call functions without parentheses or brackets. Doing so, the code looks much more like a natural language.

* What's the difference between lazy and lateinit?

lateinit means to initialize value later in code

lazy can be assigned to val but value in lazy is set at runtime

* object can be used to create singleton class

* static variables and method can be defined using companion object

* Array can defined using arrayOf(1,2,3)

* Java vs kotlin

1. kotlin removes boilerplate code
2. lambda expression just like java 1.8
3. 40% less coding

* how do you declare a variable as volatile in kotlin?

>By providing @volatile before variable declaration.

* Ternary conditional operator can be defined using if condition

* There is dependency of secondary constructor on primary constructor.

* How do you think extension functions are useful?

Extension functions helps to extend a class with new functionality without having to inherit from class.

* instanceof in kotlin works like object1 is object2

* way to define for loop in range

```
for(i in 1..15){
}
```

* kotlin doesn't support primitive datatype

* kotlin can be executed without JVM

https://github.com/siddhpatil6/Kotlin/wiki/Android-Interview-Questions