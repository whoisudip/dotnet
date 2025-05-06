TRIBHUVAN UNIVERSITY
2018

Group B

Attempt any Six questions :
[5x6=30]

2. What is CLR? List and explain the features of CLR.

3. What do you mean by value type and reference type? Give an example for each.

4. What is an interface? How interface is used in multiple inheritance? Explain with example.

5. Why namespace is used in C#? How to create and use the namespace in C#? Explain with example.

6. What is an Exception? Write a program to generate divide by zero exception and index out of range exception and also handle these exceptions.

7. What is a Query expression? Write a C# program to select Students who are lived in Kirtipur and studied in Patan Multiple Campus using LINQ.

8. What do you mean by static class and constructor? Explain with suitable example.

Group C

Attempt any Two questions:
[10x2=20]

9. What do you mean by operator overloading? Write a C# program to demonstrate binary and relational operator overloading.

10. Explain difference between ExecuteReader and ExecuteNonQuery. Provided that a mysql database named "Company" with table named "Product" with following columns (ProductId as int, ProductName as varchar(20), and UnitPrice as float). Write a c# program to connect to the database and display product records that have UnitPrice is greater than RS. 1000 and update the product record (such as UnitPrice=4500) from product database whose ProductId=50.

11. What is web server control in ASP.NET? List few web server control used in ASP.NET. Write a program to create student registration form in one ASP.NET page and display the filled data with another page.

---

### 📘 **DotNet Technology – 2024 (Tribhuwan University)**

**Group B – Attempt any SIX questions. \[6x5 = 30]**

1. What is the importance of Garbage Collection in .NET Framework? Explain .NET Framework architecture with suitable diagram.
2. What is variable size array? Write a C# program to create a multidimensional array to store the marks of three students in different subjects.
3. Explain the concept of static class and static constructor with a suitable program.
4. What is named argument? Explain with a suitable program how to create alias for namespace in C#.
5. What is static binding? Write a C# program to add and subtract two complex numbers using binary operator overloading.
6. Why is Delegate used in C#? Write a C# program to select odd and divisible by 3 numbers from list (1–30) using LINQ.
7. Write short notes on (any two):
   a) Copy constructor
   b) Indexer
   c) Lambda Expression

**Group C – Attempt any TWO questions. \[2x10 = 20]**

8. Differentiate between struct and enum. Why handle exceptions? Illustrate with your own custom exception.
9. What is generics? Explain with example. How is virtual method used to achieve polymorphism?
10. What is DataReader in ADO.NET? Design an application scenario.

---

### 📘 **DotNet Technology – 2021 (Tribhuwan University)**

**Group B – Attempt any SIX questions. \[6x5 = 30]**

1. What do you mean by C# as a type-safe language? Explain any four applied technologies in .NET.
2. List any five contextual keywords in C#. Write a C# program to initialize and display jagged array with sum of each row.
3. What is string interpolation? How does passing argument by value differ from reference? Explain with program.
4. What are the uses of the `base` keyword in C#? Write a C# program with class and abstract method.
5. What is virtual method? Write a C# program illustrating multilevel inheritance.
6. Difference between indexer and properties? Explain generics with a suitable program.
7. Write a program to create a form for calculating simple interest in one ASP.NET page and display it in another.

**Group C – Attempt any TWO questions. \[2x10 = 20]**

8. a) What is SystemException? Write a C# program that reads balance and withdrawal amount; throw ApplicationException if withdrawal > balance.
   b) List five LINQ standard operators. Write a C# program to sort employees by salary descending using LINQ.

9. What are different types of delegates in C#? Write a C# program to create a class using delegate.

---

### 📘 **DotNet Technology – 2020 (Tribhuwan University)**

**Group B – Attempt any SIX questions. \[6x5 = 30]**

1. Differentiate Object-Oriented Programming and Object-Based Programming. Explain features of C#.
2. Explain Microsoft .NET Framework and its components.
3. What is a property in C#? How is it different from a method? Compare automatic vs normal property with example.
4. Define constructor. Explain types of constructors in C# with example.
5. Define inheritance. Write a C# program demonstrating multilevel and multiple inheritance.
6. What is generics? List types of generic classes. Explain delegate with example.
7. What is a lambda expression? Explain types used in C# with examples.

**Group C – Attempt any TWO questions. \[2x10 = 20]**

8. a) Write a program to create user registration form in one ASP.NET page and display filled data in another.
   b) Write a program to handle exception in ASP.NET.

9. a) How is virtual method used for dynamic binding in C#? Explain with program.
   b) Define operator overloading. Write a C# program to overload binary operator.
   
10. a) What is LINQ? Write a program to select employees with salary > 20000 and address = Kathmandu using LINQ.
    b) Write a C# program to show insert and select operations in a database.

---

##ANSWERS
##XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX



Great, I will prepare exam-style answers from Tribhuvan University's DotNet Technology exam papers (2018–2024), including only Group B and Group C questions that are not related to databases or web technologies. Answers will be clearly marked by question and marks (\[5 Marks], \[10 Marks]), written in simple, clear, university-level English.

I'll let you know as soon as it's ready.


# DotNet Technology (C#) Exam Questions – Group B & C

## CLR and .NET Architecture \[10 Marks]

**Definition:** The **Common Language Runtime (CLR)** is the core execution engine of the .NET Framework. It is a virtual machine that manages execution of .NET programs written in C#, VB.NET, F#, etc. When C# code is compiled, it generates Intermediate Language (IL) code (also called MSIL) that is platform-independent. At runtime, the CLR’s **JIT compiler** translates this IL into native machine code. The CLR also provides a managed execution environment with services such as memory management, garbage collection, type checking, security, and exception handling.

**Importance in C#:** CLR is crucial because it automates many low-level tasks. It **automatically manages memory** through garbage collection, which prevents memory leaks and frees developers from manual memory management. It enforces **type safety** by using the Common Type System (CTS) and Common Language Specification (CLS), ensuring that objects from different languages interoperate safely. It also provides **cross-language integration**, allowing C# code to work seamlessly with libraries written in other .NET languages. Thus, the CLR enables the “managed code” environment of .NET, improving reliability and security.

**Example/Diagram:** A high-level view of .NET architecture:

* **Application Code (C# source)** is compiled into **IL/CLI code**.
* The **CLR** loads the IL, compiles it with the **JIT compiler** into native code, and executes it.
* **Base Class Libraries (BCL)** provide common APIs (collections, IO, etc.) used by the code.
* CLR services (Garbage Collector, Security Manager, Exception Manager) run alongside.

No code example is needed for CLR, but conceptually:

```text
C# source → (C# Compiler) → IL/CLI code → (CLR + JIT) → Native machine code on execution:contentReference[oaicite:6]{index=6}:contentReference[oaicite:7]{index=7}.
```

## Value Types vs Reference Types \[5 Marks]

**Definition:** In C#, types are divided into **value types** and **reference types**. A *value type* (e.g. `int`, `struct`, `enum`) directly contains its data. A *reference type* (e.g. `class`, `string`, `array`) stores a reference (pointer) to the actual data object. In other words, a value type variable holds the data itself, whereas a reference type variable holds the address of the data.

**Importance in C#:** The distinction affects how data is passed and copied. When you assign or pass a value type, a **new copy** of the data is made, so changes to one copy do not affect another. For example:

```csharp
int a = 5;
int b = a;
b = 10;
// a is still 5, b is 10
```

This shows that `b` got a separate copy of the value 5. On the other hand, reference types share references. If two variables reference the same object, changes via one variable affect the same object:

```csharp
class Point { public int X; }
Point p1 = new Point { X = 1 };
Point p2 = p1;
p2.X = 5;
// Now p1.X is also 5, because p1 and p2 reference the same object.
```

Thus, understanding value vs reference is important for predicting behavior of assignments, method calls, and memory usage. Value types are generally stored on the stack and are efficient for small data, while reference types are on the heap and useful for complex objects.

## Interfaces and Multiple Inheritance \[10 Marks]

**Definition:** An **interface** in C# is a reference type that defines a contract of methods, properties, or events without implementation. Any class or struct that implements an interface must provide concrete implementations for its members. C# does **not** support multiple class inheritance (a class inheriting from more than one class). Instead, it allows a class to implement multiple interfaces. This is a form of *multiple inheritance of types* through interfaces. In other words, a C# class can inherit from one base class (single inheritance) but can implement many interfaces to achieve multiple inheritance of capabilities.

**Importance in C#:** Interfaces are important for abstraction and polymorphism. They allow different classes to share a common set of method signatures. For example, if two unrelated classes implement the same interface, they can be used interchangeably through that interface. Implementing multiple interfaces allows a class to promise support for multiple behaviors or contracts. This overcomes the limitation of single class inheritance. For instance:

```csharp
interface IDraw { void Draw(); }
interface IColor { string GetColor(); }

class Rectangle : IDraw, IColor {
    public void Draw() { /* draw rectangle */ }
    public string GetColor() { return "Blue"; }
}

Rectangle rect = new Rectangle();
rect.Draw();
Console.WriteLine(rect.GetColor());
```

Here, `Rectangle` implements two interfaces, inheriting the contract of both. This provides flexibility: "allows a class to inherit from multiple sources". The interface-enforced contracts ensure consistency in the codebase.

**Example (Multiple Inheritance using Interfaces):** Even though C# forbids multiple class inheritance, a class can implement multiple interfaces. For example, if `IShape` and `IColor` are interfaces, then:

```csharp
interface IShape { double GetArea(); }
interface IColor { string GetColor(); }

class Rectangle : IShape, IColor {
    public double Width, Height;
    public Rectangle(double w, double h) {
        Width = w; Height = h;
    }
    public double GetArea() { return Width * Height; }
    public string GetColor() { return "Red"; }
}
```

This `Rectangle` class implements both interfaces, effectively combining multiple behaviors. A diagram of class inheritance would show `Rectangle` inheriting from (or implementing) both interface contracts.

*Cited:* C# does not support multiple class inheritance, but a class can implement multiple interfaces to achieve multiple inheritance of functionality. Interfaces enforce a contract that implementing classes must adhere to.

## Namespaces \[5 Marks]

**Definition:** A **namespace** in C# is a named grouping of related classes, interfaces, enums, and other types. It helps organize code and prevent name conflicts. For example, you might have `namespace Utilities { class Helper { } }`. Namespaces create a scope for identifiers. According to GeeksforGeeks, namespaces provide a way to keep one set of names (like class names) different from another set of names.

**Importance in C#:** Namespaces are essential in large projects to manage code. They **prevent naming collisions**: two classes with the same name in different namespaces are treated as distinct types. For instance, `MyCompany.ProjectA.Logger` and `MyCompany.ProjectB.Logger` can coexist if in different namespaces. Namespaces also improve code readability by grouping related classes. The C# `using` directive can import a namespace so you don’t have to fully qualify type names.

**Example:**

```csharp
namespace MyApplication.Models {
    class Person {
        public string Name;
    }
}
namespace MyApplication.Utilities {
    class Person {  // Different class, same name but different namespace
        public void Display(string name) { Console.WriteLine(name); }
    }
}
```

Here `Models.Person` and `Utilities.Person` are distinct because of their namespaces. You can refer to them by their fully qualified names or use `using MyApplication.Models;`.

## Exception Handling \[10 Marks]

**Definition:** **Exception handling** in C# is the mechanism to deal with runtime errors (exceptions) using `try`, `catch`, and `finally` blocks. When code in a `try` block throws an exception, the CLR looks for a matching `catch` block to handle it. The `finally` block (if provided) executes code after try/catch, regardless of whether an exception occurred. Exception handling allows a program to respond to error conditions and continue or terminate gracefully.

**Importance in C#:** Without exception handling, runtime errors would crash the program abruptly. Using `try-catch`, a program can **recover or fail gracefully**. For example, catching a `FormatException` during user input lets you prompt the user again instead of crashing. Proper exception handling also helps in resource management (e.g., closing files in `finally` or using `using`). According to Microsoft, a `try` block is used to partition code that might cause an exception, and `catch` blocks handle the exceptions.

**Example:**

```csharp
try {
    int number = int.Parse("abc"); // This will throw FormatException
    Console.WriteLine(number);
}
catch (FormatException ex) {
    Console.WriteLine("Input was not a valid number.");
}
finally {
    Console.WriteLine("Try-catch block has completed.");
}
```

In this example, when parsing fails, the `catch` block handles the `FormatException`. The program does not crash; instead it prints an error message and continues. This illustrates using try-catch to handle exceptions gracefully.

## Static Class and Static Constructor \[5 Marks]

**Definition (Static Class):** A **static class** in C# is a class that can only contain static members (methods, fields, properties, etc.) and cannot be instantiated. You cannot use `new` on a static class. Static classes are implicitly sealed (cannot be inherited) and are loaded by the CLR when first used. An example from .NET is the `System.Math` class, which contains only static methods and cannot be instantiated.

**Definition (Static Constructor):** A **static constructor** is a special constructor that initializes static members of a class. It has no access modifiers and no parameters, and it is called automatically by the runtime *once*, before the class is first used. Static constructors are useful for initializing static data or performing actions that need to happen only once.

**Importance/Usage:** Static classes are useful as utility or helper classes that group related methods. For example, a `UtilityClass` with methods `DoWork()` might be static. Since no instances are created, members are accessed with `UtilityClass.DoWork()`. This enforces that no instance state exists. Static constructors ensure that expensive or one-time initialization is done before the class is used. The CLR guarantees that the static constructor is called once before any static member access.

**Example:**

```csharp
static class MathUtility {
    // Static constructor
    static MathUtility() {
        // One-time initialization code, if needed
    }
    public static int Add(int a, int b) {
        return a + b;
    }
}

// Usage:
int sum = MathUtility.Add(3, 4);  // No need to create an object
```

Here, `MathUtility` is static (cannot be instantiated) and has a static method `Add`. The static constructor (if present) would run once before any call to `Add`.

## Operator Overloading \[5 Marks]

**Definition:** **Operator overloading** in C# allows you to define custom behavior for built-in operators when applied to user-defined types (classes or structs). For example, you can overload the `+` operator in a `ComplexNumber` class so that `c1 + c2` adds complex numbers meaningfully. In code, this is done by declaring a special method using the `operator` keyword inside the class.

**Importance in C#:** Overloading operators makes user-defined types easier to work with by giving them intuitive syntax. Instead of calling a method like `Add(c1, c2)`, you can write `c1 + c2`. It “provides additional capabilities to C# operators when they are applied to user-defined data types”. However, only certain operators can be overloaded, and overloading should make the code more readable and logical.

**Example:** Overloading the `+` operator for a simple `Point` struct:

```csharp
public struct Point {
    public int X, Y;
    public Point(int x, int y) { X = x; Y = y; }
    // Overload the + operator to add two points
    public static Point operator +(Point p1, Point p2) {
        return new Point(p1.X + p2.X, p1.Y + p2.Y);
    }
}
...
Point a = new Point(1, 2);
Point b = new Point(3, 4);
Point c = a + b;  // Uses overloaded + operator
Console.WriteLine($"({c.X}, {c.Y})"); // Outputs (4, 6)
```

In this example, `operator +` is defined to add the coordinates of two `Point` instances. According to GeeksforGeeks, “operator overloading gives the ability to use the same operator to do various operations” on user-defined types.

## Delegates \[5 Marks]

**Definition:** A **delegate** in C# is a type-safe object that holds a reference to a method. It is similar to a function pointer in C/C++, but is object-oriented and type-safe. A delegate’s signature defines the return type and parameters of the methods it can reference. For example, `public delegate void MyDelegate(string message);` declares a delegate type that can point to any method taking a `string` and returning `void`.

**Importance in C#:** Delegates are the foundation for callback methods and events. They allow methods to be passed as parameters, enabling flexible designs and asynchronous programming. Once you instantiate a delegate with a method, calling the delegate will invoke that method. As Microsoft notes, delegates are “object-oriented, type safe, and secure” encapsulations of methods. Delegates are used extensively in LINQ and async programming (`Func<T>` and `Action<T>` are generic delegates), as well as for defining event handlers.

**Example:**

```csharp
// Declare a delegate type
public delegate void PrintMessage(string msg);

// A method matching the delegate signature
public static void Show(string text) {
    Console.WriteLine(text);
}

static void Main() {
    // Instantiate the delegate, pointing to Show method
    PrintMessage printer = Show;
    // Invoke the delegate, which calls Show
    printer("Hello from delegate!");
}
```

Here `PrintMessage` is a delegate type. We assign `Show` to it and call `printer("...")`. According to Microsoft, “A delegate is a type that safely encapsulates a method”.

## LINQ Queries (in-memory collections) \[10 Marks]

**Definition:** **LINQ** (Language Integrated Query) is a set of C# language features and libraries that allow writing SQL-like queries over in-memory data collections (arrays, lists, XML, etc.) using C# syntax. With LINQ, developers can use query expressions (or lambda expressions) to filter, sort, and project data from collections consistently. As Microsoft states, LINQ “offers a consistent C# language model for kinds of data sources and formats,” and you always work with C# objects in a LINQ query.

**Importance in C#:** LINQ simplifies data manipulation without requiring loops or external query languages. It promotes readable, concise code. For example, you can query an array of integers to find even numbers in one line. Because LINQ queries work with any `IEnumerable<T>` (in-memory collections), they are not tied to databases here. LINQ methods (like `Where`, `Select`) or query syntax (`from ... in ... where ... select ...`) make code easier to maintain.

**Example:** Using LINQ to filter an integer array:

```csharp
int[] numbers = { 0, 1, 2, 3, 4, 5, 6 };
// Query syntax
var evens = from num in numbers
            where num % 2 == 0
            select num;
// Execution of the query
foreach(int num in evens) {
    Console.Write(num + " ");  // Output: 0 2 4 6
}
```

This illustrates the three parts of a LINQ query (data source, query creation, execution). All numbers in `numbers` are C# objects, and the query returns even ones. Microsoft’s example shows exactly this pattern. LINQ queries are flexible and can be applied to lists, arrays, or any collection, making data querying more uniform across different data sources.

## Structs vs Enums \[5 Marks]

**Definition (Struct):** A **struct** in C# is a user-defined value type that can contain data and related functionality. It is defined with the `struct` keyword. Structs are usually used for small, lightweight objects. Unlike classes, structs are allocated on the stack (when used as local variables) and hold their data directly. A struct can have fields, methods, properties, and constructors.

**Definition (Enum):** An **enum** is a distinct value type that consists of a set of named constant values. Each enum member has an underlying integer (by default `int`) value. Enums are useful for defining a group of related constants (such as days of the week, months, etc.) with meaningful names.

**Importance in C#:** Both structs and enums are value types, meaning they store data directly. Structs are used when you need a small object type without the overhead of a class. For example, `System.Drawing.Point` is a struct representing X,Y coordinates. Because structs are value types, they get copied on assignment, which can be more efficient for small data. Enums improve code readability by replacing “magic numbers” with names; they also make code safer by limiting values to a defined set.

**Example:**

```csharp
// A struct definition
public struct Point { 
    public int X, Y; 
    public Point(int x, int y) { X = x; Y = y; }
}

// An enum definition
public enum Day { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday }

// Usage
Point p = new Point(2, 3);
Day today = Day.Wednesday;
Console.WriteLine($"Point is at ({p.X}, {p.Y}), Today is {today}");
```

Here `Point` is a struct (value type with two fields), and `Day` is an enum (a named list of integer constants). As summarized: “Structs and enums are both specialized value types in C#.” Structs can have methods and constructors, while enums assign names to integer values.

## Generics \[10 Marks]

**Definition:** **Generics** in C# allow the definition of classes, methods, interfaces, and delegates with placeholders for the data type. Using generics, you declare a *type parameter* (commonly `T`) so that the code works for any data type specified when the class or method is used. For example:

```csharp
public class GenericList<T> {
    public void Add(T item) { /* ... */ }
}
```

This `GenericList<T>` can then be used as `GenericList<int>`, `GenericList<string>`, etc. Generics enable **type parameters** so that types can be specified later.

**Importance in C#:** Generics provide *reusability* and *type safety*. A generic class/method can work with any data type without the need for casts or boxing. For example, instead of using non-generic collections like `ArrayList` (which stores `object`), you use `List<T>`, which enforces compile-time type checking. Microsoft documentation notes that generics allow code reuse without runtime casts or boxing. They also improve performance by avoiding boxing (for value types) and avoid runtime errors from invalid casts. Generics are heavily used in .NET collections (e.g., `List<T>`, `Dictionary<TKey,TValue>`) and in LINQ (`Func<T>`, `IEnumerable<T>`).

**Example:** A simple generic class and its usage:

```csharp
// Generic class with type parameter T
public class Box<T> {
    public T Value;
    public Box(T value) { Value = value; }
}

// Using the generic class with different types
Box<int> intBox = new Box<int>(123);
Box<string> strBox = new Box<string>("hello");
Console.WriteLine(intBox.Value);  // 123
Console.WriteLine(strBox.Value);  // hello
```

At compile time, `T` is replaced with the actual type (`int` or `string`). This shows reusability (same code for multiple types) and type safety (no need to cast from `object`). The cited example in Microsoft documentation explains how generics “combine reusability, type safety, and efficiency”.

## Virtual Methods \[5 Marks]

**Definition:** A **virtual method** in C# is a method declared in a base class with the `virtual` keyword, allowing derived classes to override it using the `override` keyword. This enables **runtime polymorphism**. When a virtual method is called on a base class reference, the CLR invokes the derived class’s override if one exists.

**Importance in C#:** Virtual methods allow writing flexible code that works with class hierarchies. You can treat all derived classes uniformly through a base class reference, and the appropriate method is called according to the object’s actual type. For example, consider a base class `Shape` with a virtual method `Draw()`, and derived classes `Circle`, `Rectangle` that override `Draw()`. You can store different shapes in a `List<Shape>` and call `Draw()` on each; the correct override runs for each shape. As Microsoft explains, the CLR looks up the runtime type and calls the appropriate override of the virtual method.

**Example:**

```csharp
class Shape {
    public virtual void Draw() {
        Console.WriteLine("Drawing a generic shape");
    }
}
class Circle : Shape {
    public override void Draw() {
        Console.WriteLine("Drawing a circle");
    }
}
...
Shape s = new Circle();
s.Draw(); // Outputs "Drawing a circle" because Circle overrides Draw().
```

Even though `s` is declared as `Shape`, the overridden `Circle.Draw()` executes at runtime. This demonstrates polymorphism via virtual methods. Microsoft notes that derived classes “can override \[virtual methods] to provide their own definition,” enabling “at run-time...derived class’s version of the method \[to be executed]”.

## Indexers and Properties \[10 Marks]

**Indexers:** An **indexer** allows an object to be indexed like an array. You define an indexer in a class/struct using the `this` keyword with a parameter. The indexer has `get` and/or `set` accessors that take parameters (usually an index). The class using the indexer then behaves like a virtual array. For example:

```csharp
class SampleCollection {
    private string[] data = new string[3];
    // Define indexer
    public string this[int index] {
        get { return data[index]; }
        set { data[index] = value; }
    }
}
...
SampleCollection col = new SampleCollection();
col[0] = "Hello";
Console.WriteLine(col[0]);  // Outputs "Hello"
```

Here `col[0]` uses the indexer. According to GeeksforGeeks, “indexers allow an instance of a class or struct to be indexed as an array”. Indexers improve usability when a class naturally represents a collection or sequence.

**Properties:** A **property** in C# is like a field with controlled access. It appears as a field to the outside, but internally has `get` and/or `set` methods. Properties encapsulate private fields and can include validation or other logic. Unlike fields, properties are methods under the hood. For example:

```csharp
class Person {
    private int age;
    public int Age {
        get { return age; }
        set {
            if (value >= 0) age = value;  // validation
        }
    }
}
```

Here `Age` is a property. Consumers of `Person` use `person.Age` like a variable, but the setter ensures `age` is non-negative. As Microsoft explains, “properties combine aspects of both fields and methods” and their get/set blocks run code on read/write. They allow you to enforce invariants (e.g., range checks) transparently.

**Importance:** Both indexers and properties provide flexible ways to access data members. Properties encapsulate data access and hide implementation, supporting encapsulation and validation. Indexers make objects act like arrays, improving intuitiveness when working with collections. For example, a `MonthTemperatures` class with an indexer lets users write `temp[0] = 30;` instead of method calls. They improve code readability and maintainability.

## Copy Constructors and Lambda Expressions \[5 Marks]

**Copy Constructor:** A **copy constructor** is a constructor that creates a new object as a copy of an existing object. In C#, you can implement one by defining a constructor that takes an object of the same class and copies its fields. For example:

```csharp
class Point {
    public int X, Y;
    public Point(int x, int y) { X = x; Y = y; }
    // Copy constructor
    public Point(Point p) {
        X = p.X;
        Y = p.Y;
    }
}
Point p1 = new Point(3, 4);
Point p2 = new Point(p1); // p2 is a copy of p1
```

A copy constructor ensures the new object has the same state as the original. It is important for creating duplicate instances, especially if the class contains references or needs a deep copy. (C# does not provide a default copy constructor, so it’s user-defined.)

**Lambda Expressions:** A **lambda expression** in C# is an anonymous function that you can use to create delegates or expression trees. It uses the `=>` operator to separate parameters and the expression or statement block. Lambdas make code concise, especially in LINQ or when passing small functions. For example, `x => x * x` is a lambda taking `x` and returning `x*x`. According to Microsoft, you use a lambda to create an anonymous function, and any lambda can be assigned to a delegate or `Func<>` type.

**Importance:** Copy constructors are useful in object-oriented designs where explicit copying of an object’s data is needed. Lambda expressions enable succinct in-place function definitions. They are heavily used with delegates and LINQ, allowing inline definitions of functionality. For instance, consider sorting a list with a custom comparison:

```csharp
List<int> numbers = new List<int>{3,1,4};
numbers.Sort((a, b) => a.CompareTo(b)); // lambda used as comparison delegate
```

Here `(a, b) => a.CompareTo(b)` is a lambda. Lambdas often make code clearer than defining separate delegate types or methods. As Microsoft notes, lambdas use `=>` and can be converted to `Func` or `Action` delegate types.

## Multilevel and Multiple Inheritance \[10 Marks]

**Multilevel Inheritance:** In C#, **multilevel inheritance** means a class is derived from a derived class. For example: `Animal → Mammal → Dog`. Here `Mammal` inherits from `Animal`, and `Dog` inherits from `Mammal`. Each level adds or extends features. As defined in GeeksforGeeks, “multilevel inheritance refers to creating a derived class from a base class, and then another derived from the first”. This forms a chain of inheritance.

**Multiple Inheritance:** C# **does not support multiple class inheritance**, meaning a class cannot inherit from more than one base class. For example, you cannot write `class C : A, B { }` if A and B are both classes. Instead, a class can implement multiple interfaces (see previous section) to achieve a form of multiple inheritance of behavior. This design avoids ambiguity issues (the “diamond problem”) found in some languages.

**Comparison:** In multilevel inheritance, inheritance is single at each level but chained. It is fully supported in C#: `class B : A { }`, `class C : B { }` is allowed. In multiple inheritance, a single class with two parent classes is disallowed. To circumvent this, C# uses interfaces (as discussed above).

**Examples:**

* *Multilevel:*

  ```csharp
  class Animal { public void Eat() { Console.WriteLine("Animal eats"); } }
  class Mammal : Animal { public void Walk() { Console.WriteLine("Mammal walks"); } }
  class Dog : Mammal { public void Bark() { Console.WriteLine("Dog barks"); } }
  ```

  Here `Dog` can `Eat()`, `Walk()`, and `Bark()`.
* *Multiple:*

  ```csharp
  interface IFly { void Fly(); }
  interface IWalk { void Walk(); }
  // Bird implements both IFly and IWalk
  class Bird : IFly, IWalk {
      public void Fly() { /*...*/ }
      public void Walk() { /*...*/ }
  }
  ```

  Although `Bird` does not inherit multiple classes, it implements multiple interfaces to combine behaviors.

*Cited:* C# fully supports multilevel inheritance but not multiple class inheritance. Multiple behaviors are achieved through interface implementation.

## Object-Oriented vs Object-Based Programming \[5 Marks]

**Definition (Object-Oriented):** An **object-oriented** language fully supports the key pillars of OOP: encapsulation, inheritance, and polymorphism. Object-oriented languages allow defining classes, creating objects, and using inheritance hierarchies. C# is a full object-oriented language: it supports classes, inheritance, polymorphism, and other OOP concepts.

**Definition (Object-Based):** An **object-based** language supports objects and encapsulation but does *not* support all OOP features like inheritance or polymorphism. Such languages let you create and use objects, but without full class inheritance hierarchies. For example, JavaScript (pre-ES6) is often called object-based: it has objects and prototypes, but it did not have classes or true inheritance (older versions).

**Difference in C#:** C# is object-oriented: it has inheritance and polymorphism. In contrast, a purely object-based language would lack inheritance. The tutorial note explains that object-based languages (like some scripting languages) support encapsulation and objects but not inheritance or polymorphism.

**Importance:** Understanding this helps categorize languages. C#, Java, and VB.NET are listed as object-oriented because they support all OOP features. In exams, note that object-based is a limited term: C# is *not* object-based, it is fully object-oriented. Object-based languages (e.g. older JavaScript) allow objects but you cannot create subclass hierarchies in the same way.

*Example Comparison:*

* C#: can do `class A { } class B : A { }` (inheritance).
* JavaScript (pre-class syntax): objects can contain methods, but you cannot say `class B extends A` (inheritance) in older versions.

*Cited:* Object-based languages support objects/encapsulation but do not support inheritance or polymorphism, whereas object-oriented languages support all OOP features including inheritance.

## String Interpolation \[5 Marks]

**Definition:** String interpolation in C# is a syntactic feature introduced in C# 6.0 that allows embedding expressions inside string literals. It uses the `$` prefix before the string, and expressions are enclosed in `{}` within the string. For example, `$"Hello {name}"` inserts the value of `name` into the string. This is “another option of string concatenation” where variable values substitute into placeholders.

**Importance in C#:** Interpolation makes formatting strings more readable and concise compared to concatenation. It automatically converts expressions to strings and handles spacing, improving code clarity. Instead of `Console.WriteLine("Name: " + firstName + " " + lastName);`, you can write:

```csharp
Console.WriteLine($"Name: {firstName} {lastName}");
```

This is clearer and less error-prone. String interpolation also supports formatting, e.g. `${value:C}` for currency. It simplifies code and enhances maintainability.

**Example:**

```csharp
string firstName = "John";
string lastName = "Doe";
string fullName = $"My full name is: {firstName} {lastName}";
Console.WriteLine(fullName);
```

This will output “My full name is: John Doe”. The `$` symbol is required as shown. String interpolation was introduced in C# 6 and is now a common way to build strings with embedded expressions.

## Named and Alias Namespaces \[5 Marks]

**Named Namespace:** A normal namespace in C# is defined using the `namespace` keyword, for example `namespace MyApp.Utilities { class Helper { } }`. It is a container for types (classes, interfaces, etc.), as described earlier.

**Alias Namespace:** C# allows creating an **alias** for a namespace (or type) using the `using` directive. This provides a shorter or disambiguated name. For example:

```csharp
using Proj = MyCompany.Product.Feature.Module;
...
Proj.MyClass obj = new Proj.MyClass();
```

Here `Proj` is an alias for the long namespace. You can also alias assembly externals. The alias qualifier `::` can be used to explicitly reference the global namespace or an alias. GeeksforGeeks explains that the namespace alias qualifier (`::`) lets you avoid ambiguous definitions by giving a shorter name to a long namespace.

**Importance:** Aliases are useful when two namespaces have types with the same name or when a namespace name is very long. For example, if two libraries both have `Tools.Logger`, you can alias one namespace (`using ToolsA = CompanyA.Tools; using ToolsB = CompanyB.Tools;`) and then use `ToolsA.Logger` and `ToolsB.Logger`. Alias qualifiers (with `::`) can explicitly refer to the global namespace or an alias.

**Example:**

```csharp
using System;
using Col = MyApp.Collection;  // Col is an alias
...
// Use alias
Col.MyCollection list = new Col.MyCollection();
```

This avoids writing the full namespace `MyApp.Collection`. The alias syntax is `using alias_name = namespace;`. If needed, you can also use `global::` to refer to the global namespace and avoid conflicts.

## Variable (Multidimensional) and Jagged Arrays \[5 Marks]

**Multidimensional Array:** A **multidimensional array** (e.g., a 2D array) is a single array with multiple dimensions, declared like `int[,] matrix = new int[3,4];`. All rows have the same length. This array is stored as one contiguous block. You access elements with comma-separated indices: `matrix[1,2]`.

**Jagged Array:** A **jagged array** is an array of arrays. It is declared with square brackets for each level: `int[][] jagged = new int[3][];`. Each element of the main array is itself a separate array, which can have different lengths. For example:

```csharp
int[][] jagged = new int[3][];
jagged[0] = new int[2] {1,2};
jagged[1] = new int[3] {3,4,5};
jagged[2] = new int[1] {6};
```

Here row 0 has length 2, row 1 has length 3, etc. According to GeeksforGeeks: *“A jagged array is an array of arrays, where each element in the main array can have a different length.”*.

**Differences/Importance:**

* **Dimensions:** Multidimensional arrays have fixed size in each dimension. Jagged arrays allow *variable-length* inner arrays.
* **Memory Layout:** Multidimensional arrays are contiguous blocks; jagged arrays are separate blocks for each sub-array.
* **Usage:** Use a multidimensional array when your data forms a regular grid (like a matrix). Use a jagged array when rows vary in length (like a triangular matrix or list of lists).
* **Example Access:** `matrix[i,j]` vs `jagged[i][j]`.

**Example Code:**

```csharp
// Multidimensional (2D) array with 2 rows, 3 columns
int[,] matrix = { {1,2,3}, {4,5,6} };
Console.WriteLine(matrix[1,2]);  // 6

// Jagged array with 2 rows
int[][] jagged = new int[2][];
jagged[0] = new int[] {10, 20};
jagged[1] = new int[] {30, 40, 50};
Console.WriteLine(jagged[1][2]); // 50
```

In the jagged example, the two rows have different lengths. A jagged array provides “flexibility: variable number of elements in each row”.


