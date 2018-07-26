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





