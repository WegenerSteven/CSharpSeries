# intro - to - C#.NET

C#.NET is a modern, object-oriented programming language developed by microsoft as part of the .NET framework. Widely
used for building web applications, desktop applications and cloud-based services.
C#.NET contains all the features of C++, VB.NET and JAVA as well as some additional features.

>C#.NET is designed to be;`Simple` `modern` `general-purpose` and `object oriented`

## objectives
1. Introduction and setup
2. C#.NET basics
3. OOPs in C#
4. Exception handling
5. Events, Delegates and lambda expressions C#
6. Multithreading
7. Collection in C#
8. File Handling
9. Asynchronous Programming
10. Parallel Programming
11. AutoMapper
12. Optional Parameter, indexes and Enums
13. .Net Framework Architecture
14. Var Dynamic and Reflection

## Why Use C#?
* It is one of the most popular programming languages in the world 
* It is easy to learn and simple to use 
* It has huge community support 
* C# is an object-oriented language which gives a clear structure to programs and allows code to be reused, lowering development costs 
* As C# is close to C, C++ and Java, it makes it easy for programmers to switch to C# or vice versa

# Basic structure of C#
![basic of c#.png](basic of c#.png)
The above process is shown in the below diagram
![structure-explain.png](structure-explain.png)
> C#.NET is a Case-sensitive Language and Every Statement in C# should end with a semicolon.

#### Explain main blocks of the program
1. **using System** - Means that we can use classes from the `System` namespace
2. **namespace** - used to organize your code, and it is a container for classes and other namespaces to avoid conflicts and for code management.
    * Prevent naming conflicts: i.e class Person can NamespaceA.Person and NamespaceB.Person
    * Built in namespaces: System which is used by console.
    * Declared using namespace keyword.
3. The curly braces `{}` marks the beginning and the end of a block of code
4. **class**: is a container for data and methods, which brings functionality to your program. 
    * Also; A class is a blueprint that defines the structure of object. Defines what an object will look like and what actions it can perform.
    * It contains fields(variables), `methods`, `properties`, `constructors` and more
      - **objects in C#**
        - An object is an instance of a class. A class does not take memory when created until an object is created
          - Features of Classes and Objects:
            - *Encapsulaton* - Bundle data and methods behavior.
            - *Abstraction* - Hiding complexity of a system.
            - *Inheritance* - Inherit from other classes to enable code reuse.
            - *Polymorphism* - Objects behave differently from their actual class.
5. **static void main()** - defines the Main method, which is the entry point for all C# programs. The `Main` method states what the class does when executed.
Only one `Main` method is allowed per class. 
---
```C#
using System;
namespace ConsoleApplication1
{
  public class Program{
    public static void Main(string[] args){
      Console.WriteLine('Hello world!');
      Console.Read();
    }
  }
}
```

> We shall dive more into classes and objects in OOP.
        ![oop.concepts](oop.concepts)