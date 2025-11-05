# variables
**Variables** are used to store data that can be referenced and manipulated throughout the program. Each variable has a name type and a value.

![variable](variable)

## Types of Variables
### Local variables
- block scope, must be initialized. These variables are declared inside the method of a class. The scope of the local variable is limited to the method.

```C#
using System;
namespace TypesOfVariables
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.Read();
        }

        public void NonStaticBlock()
        {
            //By Default, every local variable is going to be non-static
            //The Scope is limited to this method only
            int x = 100;
        }

        public static void StaticBlock()
        {
            //By Default, every local variable is going to be static
            //The Scope is limited to this method only
            int y = 100;
        }
    }
}
```
### Instance variables
- declared inside a class, accessible to all methods
### Static variables
- use static keyword, shared to all objects in a class.

  *example one*
```C#
using System;
namespace TypesOfVariables
{
internal class Program
{
static int x; //Static Variable
int y; //Non-Static or Instance Variable
static void Main(string[] args)
{
int z; //Static Variable
}
}
}
```
*Example two*
```C#
using System;
namespace TypesOfVariables
{
    internal class Program
    {
        static int x = 100; //Static Variable
        int y = 200; //Non-Static or Instance Variable
        static void Main(string[] args)
        {
            Console.WriteLine($"x value: {x}");
            Console.WriteLine($"x value: {y}");
            Console.Read();
        }
    }
}
```
`Output: Compile Error`
![compile-error](compile-error)
>>Reason: memory for the variable y is going to be created only when we create an instance of the class Program and for each instance. But x does not require an instance of the class. The reason is a static variable is initialized immediately once the execution of the class starts.
### constant variables
- declared with const keyword, must be initialized, cannot be changed. `It is mandatory to initialize the constant variable at the time of its declaration only.`
```c#
 const float PI = 3.14f; 
 ```
> Constant variables are going to be created once and only one time. We cannot modify the constant values once after its declaration,
```c#
using System;
namespace TypesOfVariables
{
    internal class Program
    {
        const float PI = 3.14f; //Constant Variable
        static int x = 100; //Static Variable
        //We are going to initialize variable y through constructor
        int y; //Non-Static or Instance Variable

        //Constructor
        public Program(int a)
        {
            //Initializing non-static variable
            y = a; 
        }

        static void Main(string[] args)
        {
            //Accessing the static variable without instance
            Console.WriteLine($"x value: {x}");
            //Accessing the constant variable without instance
            Console.WriteLine($"PI value: {PI}");

            Program obj1 = new Program(300);
            Program obj2 = new Program(400);
            //Accessing Non-Static variable using instance
            Console.WriteLine($"obj1 y value: {obj1.y}");
            Console.WriteLine($"obj2 y value: {obj2.y}");
            Console.Read();
        }
    }
}
```
### Read-Only Variables
- declared with `readonly` keyword, assigned a value in a constructor. when we declare a variable by using readonly keyword, then it is known as a `readonly variable` and they can't be modified like constants but after initialization.
>The behavior of read-only variables will be similar to the behavior of non-static variables in C#, i.e. initialized only after creating the instance of the class and once for each instance of the class is created. That means we can consider it as a non-static variable and to access readonly variables we need an instance.

**Example**: `In the example below, read-only variable z is not initialized with any value but when we print the value
of the variable, the default value of int i.e 0 will be displayed.`
```C#
using System;
namespace TypesOfVariables
{
    internal class Program
    {
        const float PI = 3.14f; //Constant Variable
        static int x = 100; //Static Variable
        //We are going to initialize variable y through constructor
        int y; //Non-Static or Instance Variable
        readonly int z; //Readonly Variable

        //Constructor
        public Program(int a)
        {
            //Initializing non-static variable
            y = a; 
        }

        static void Main(string[] args)
        {
            //Accessing the static variable without instance
            Console.WriteLine($"x value: {x}");
            //Accessing the constant variable without instance
            Console.WriteLine($"PI value: {PI}");

            Program obj1 = new Program(300);
            Program obj2 = new Program(400);
            //Accessing Non-Static variable using instance
            Console.WriteLine($"obj1 y value: {obj1.y} and Readonly z value: {obj1.z}");
            Console.WriteLine($"obj2 y value: {obj2.y} and Readonly z value: {obj2.z}");
            Console.Read();
        }
    }
}
```
**Output**:   ![output](output)

**Example 2**:
`In this example we are initializing the readonly through the class constructor. Now, the constructor takes two parameters.
The first parameter will initialize the non-static variable and the second parameter will initialize the readonly variable. So,
while creating the instance, we need to pass two integer values to the constructor function.`

```c#
using System;
namespace TypesOfVariables
{
    internal class Program
    {
        const float PI = 3.14f; //Constant Variable
        static int x = 100; //Static Variable
        //We are going to initialize variable y through constructor
        int y; //Non-Static or Instance Variable
        readonly int z; //Readonly Variable

        //Constructor
        public Program(int a, int b)
        {
            //Initializing non-static variable
            y = a;
            //Initializing Readonly variable
            z = b;
        }

        static void Main(string[] args)
        {
            //Accessing the static variable without instance
            Console.WriteLine($"x value: {x}");
            //Accessing the constant variable without instance
            Console.WriteLine($"PI value: {PI}");

            Program obj1 = new Program(300, 45);
            Program obj2 = new Program(400, 55);
            //Accessing Non-Static variable using instance
            Console.WriteLine($"obj1 y value: {obj1.y} and Readonly z value: {obj1.z}");
            Console.WriteLine($"obj2 y value: {obj2.y} and Readonly z value: {obj2.z}");
            Console.Read();
        }
    }
}
```
**Output**: ![output2.png](output2.png)

For better understanding of the above example, check below diagram which shows memory representation.
![example.png](example.png)

## Rules for variable declaration in C#
- A variable name must begin with a letter or underscore.
- Variables in C# are case-sensitive
- They can be constructed with digits and letters.
- No special symbols are allowed other than underscores.
- sum, Height, _value, and abc123, etc. are some examples of the variable name