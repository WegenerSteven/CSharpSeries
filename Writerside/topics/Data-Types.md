# Data Types

**|What is a Data Type in C#**.

The data types are something that gives information about;
1. *Size* of the memory location.
2. The *Range of data* that can be stored inside that memory location
3. Possible *Legal Operations* that can be performed on that memory location. 
4. What *Types of Results* come out from an expression when these types are used inside that expression?

## Different types of Data Types Available in C#
A data type in C# specifies the type of data that a variable can store such as integer, floating, boolean, character, string, etc. 

The following diagram shows the different types of data types available in C#.

![DataTypes.png](DataTypes.png)

C# mainly categorized data types in two types: `Value types` and `Reference types`
   - `Value type` include simple types (such as int, float, bool, and char), enum types, struct types, and Nullable value types. 
   - `Reference types` includes className types, interface types, delegate types, and array types. Learn about value types and reference types in detail in the next chapter.
![datatypes.png](datatypes)

## Reference Data Type in C#
Data type which is used to store the reference of a variable is called `Reference Data Type`. In Simple terms, we can say
that the reference types do not store the actual data stored in a variable, rather they store the reference to the variables.
Reference Data types are categorized into 2 types;

    1. Predefined Types
    2. User-defined Types
### Predefined Data Types in C#
C# includes some predefined value types and reference types. 

The following table lists predefined data types:
![datatypesTable.png](datatypesTable.png)

>As you can see in the above table that each data type (except string and object) includes value range.
>The compiler will give an error if the value goes out of datatype's permitted range. For example, int data type's range is -2,147,483,648 to 2,147,483,647. So if you assign a value which is not in this range, then the compiler would give an error.

```c#
// compile time error: Cannot implicitly convert type 'long' to 'int'.
int i = 21474836470;
```
The value of unsigned integers, long, float, double, and decimal type must be suffix by u,l,f,d, and m, respectively.
```C#
uint ui = 100u;
float fl = 10.2f;
long l = 45755452222222l;
ulong ul = 45755452222222ul;
double d = 11452222.555d;
decimal mon = 1000.15m;
```
## Pointer Data Type
Pointer in C# is a variable, it is also known as a locator or indicate that points to an address of the value which means
pointer-type variables stores the memory address of another type. To get the pointer details we have two symbols ampersand(&) and asterisk(*).
    
    1. ampersand (&): It is known as Address Operator. It is used to determine the address of a variable.
    2. asterisk (*): It is also known as Indirection Operator. It is used to access the value of an address.