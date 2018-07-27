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

-----
#Data Structure

* Array - ?

* Singly Linked List - Each node in linked list contains data and a pointer. A pointer is a reference to the next item in the linked list. A linked list contains both a head and a tail.

```
class SinglyLinkedList {
        Node start;
        Node end;
        int size;

        public SinglyLinkedList() {
            start = null;
            end = null;
            size = 0;
        }

        boolean isEmpty() {
            return start == null;
        }

        public int getSize() {
            return size;
        }

        public void insertAtStart(int val) {
            Node nptr = new Node(val, null);
            size++;
            if (start == null) {
                start = nptr;
                end = start;
            } else {
                nptr.setLink(start);
                start = nptr;
            }
        }

        public void insertAtEnd(int val) {
            Node nptr = new Node(val, null);
            size++;
            if (start == null) {
                start = nptr;
                end = start;
            } else {
                end.setLink(nptr);
                end = nptr;
            }
        }

        public void insertAtPos(int val, int pos) {
            Node nptr = new Node(val, null);
            Node ptr = start;
            pos = pos - 1;
            for (int i = 1; i < size; i++) {
                if (i == pos) {
                    Node tmp = ptr.getLink();
                    ptr.setLink(nptr);
                    nptr.setLink(tmp);
                    break;
                }
                ptr = ptr.getLink();
            }
            size++;
        }

        public void deleteAtPos(int pos) {
            if (pos == 1) {
                start = start.getLink();
                size--;
                return;
            }
            if (pos == size) {
                Node s = start;
                Node t = start;
                while (s != end) {
                    t = s;
                    s = s.getLink();
                }
                end = t;
                end.setLink(null);
                size--;
                return;
            }
            Node ptr = start;
            pos = pos - 1;
            for (int i = 1; i < size; i++) {
                if (i == pos) {
                    Node tmp = ptr.getLink();
                    tmp = tmp.getLink();
                    ptr.setLink(tmp);
                    break;
                }
                ptr = ptr.getLink();
            }
            size--;
        }

        public void display() {
            System.out.println("Singly Linked list:");
            if (size == 0) {
                System.out.print("empty");
                return;
            }
            if (start.getLink() == null) {
                System.out.println(start.getData());
            }
            Node ptr = start;
            System.out.print(start.getData() + "->");
            ptr = start.getLink();
            while (ptr.getLink() != null) {
                System.out.print(ptr.getData() + "->");
                ptr = ptr.getLink();
            }
            System.out.print(ptr.getData() + "\n");
        }
    }

    class Node {
        int data;
        Node link;

        public Node() {
            link = null;
            data = 0;
        }

        public Node(int d, Node n) {
            data = d;
            link = n;
        }

        public int getData() {
            return data;
        }

        public void setData(int data) {
            this.data = data;
        }

        public Node getLink() {
            return link;
        }

        public void setLink(Node link) {
            this.link = link;
        }
    }
```

* DoublyLinkedList - A DoublyLinkedList is based on a linkedList, but there is two pointers in each node. Pointer is linked to previous and last. Last Node's next reference is null.

* Stack 

* Queue

* Sets

* Maps

* Hash Tables

* Binary Tree 

* Binary Search tree

* Heap

* Hashing

* Graph

* Matrix

* Advanced Data Structure

-----

#Android

* Difference between activity and Fragment?

An Activity is an component that provides a screen, with which users acn interact in order to do something. 

Whereas a Fragment represents a behaviour or a portion of user interface in an activity

-----

#Java

* What is difference between interfaces and abstract class?

1. An Interface is a contract. 
2. An interface is an empty shell.
3. Interface only contains abstract methods.
4. Contains only final and static variables.
5. All methods should be public
6. Interface can extend mutiple interface

--

1. Abstract classes unlike interfaces are classes.
2. Abstract classes look a lot like interfaces.