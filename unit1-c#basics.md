
---

## 1. Introduction to .NET Architecture

### 1.1 What is .NET?
- **.NET** is a developer platform created by Microsoft for building various types of applications (desktop, web, mobile, gaming, IoT, etc.).  
- It provides a collection of libraries and a runtime (the Common Language Runtime, or **CLR**) for executing applications written in different languages (C#, VB.NET, F#).

### 1.2 Common Language Runtime (CLR)
- **CLR** is the execution environment that handles:
  - Memory management (via Garbage Collection)
  - Exception handling
  - Security
  - Just-In-Time (JIT) compilation from Intermediate Language (IL) to machine code

### 1.3 Common Type System (CTS)
- Defines how types (classes, structs, enums, etc.) are declared, used, and managed.  
- Ensures that objects written in different .NET languages can interact with each other.

### 1.4 Common Language Specification (CLS)
- A set of rules that language compilers must follow so that .NET languages are interoperable.

### 1.5 Assembly
- A **.NET Assembly** is a compiled code library for deployment, versioning, and security.  
- Can be an **EXE** (executable) or **DLL** (library).  
- Contains metadata (manifest) and IL code.

---

## 2. Class and Object in C#

### 2.1 Class
- A **class** is a blueprint or template for creating objects.  
- It encapsulates data (fields) and behaviors (methods).  
- Syntax example:
  ```csharp
  public class Person
  {
      // Fields (variables)
      private string name;
      private int age;

      // Methods
      public void SetDetails(string name, int age)
      {
          this.name = name;
          this.age = age;
      }

      public void PrintDetails()
      {
          Console.WriteLine($"Name: {name}, Age: {age}");
      }
  }
  ```

### 2.2 Object
- An **object** is an instance of a class.  
- It is allocated on the managed heap when you use the `new` keyword.  
- Example of creating an object:
  ```csharp
  Person person1 = new Person();
  person1.SetDetails("Alice", 30);
  person1.PrintDetails();
  ```

---

## 3. Creating a Class

1. **Define the class**: Use the `class` keyword.  
2. **Specify access modifiers**: Typically `public` if you want it accessible outside the assembly.  
3. **Add fields, properties, methods**: These represent data and behavior.  
4. **Constructor**: Special method called automatically when an object is created.

Example:
```csharp
public class Student
{
    // Fields
    private int rollNumber;
    private string name;

    // Constructor
    public Student(int rollNumber, string name)
    {
        this.rollNumber = rollNumber;
        this.name = name;
    }

    // Method
    public void DisplayInfo()
    {
        Console.WriteLine($"Roll No: {rollNumber}, Name: {name}");
    }
}
```

---

## 4. Interface

### 4.1 What is an Interface?
- An **interface** is a contract that defines a set of methods and/or properties but does not provide an implementation.  
- A class that implements an interface must provide concrete implementations of all interface members.

### 4.2 Defining and Implementing an Interface
```csharp
public interface IAnimal
{
    void MakeSound();
}

public class Dog : IAnimal
{
    public void MakeSound()
    {
        Console.WriteLine("Bark!");
    }
}
```
- Interfaces support multiple inheritance: a class can implement multiple interfaces.

---

## 5. Creating Objects

- In C#, you create objects using the `new` keyword followed by the constructor of the class.
- You can also have **anonymous types** (for quick data grouping without a formal class), but typically you use classes.
  
Example:
```csharp
Dog dog1 = new Dog();
dog1.MakeSound(); // Output: "Bark!"
```

---

## 6. Access Modifiers

1. **public**: Accessible from anywhere.
2. **private**: Accessible only within the same class.
3. **protected**: Accessible within the same class or derived classes.
4. **internal**: Accessible within the same assembly.
5. **protected internal**: Accessible within the same assembly or any derived class.
6. **private protected**: Accessible within the same class or derived classes within the same assembly (C# 7.2+).

Example usage:
```csharp
public class Example
{
    private int x;
    protected int y;
    public int z;

    internal void SomeMethod() { /* ... */ }
}
```

---

## 7. Arrays

### 7.1 What is an Array?
- A collection of items stored at contiguous memory locations.  
- Fixed in size once declared.

### 7.2 Declaration and Initialization
```csharp
int[] numbers = new int[5];           // Declares an array of length 5
numbers[0] = 10;
numbers[1] = 20;

int[] nums = { 1, 2, 3, 4, 5 };       // Inline initialization
```

### 7.3 Multi-Dimensional Arrays
```csharp
int[,] matrix = new int[2,3];  // 2 rows, 3 columns
```

### 7.4 Jagged Arrays
```csharp
int[][] jaggedArr = new int[3][];
jaggedArr[0] = new int[2];
jaggedArr[1] = new int[5];
jaggedArr[2] = new int[3];
```

---

## 8. Inheritance

### 8.1 What is Inheritance?
- Mechanism where one class (derived or child) acquires the properties and behaviors of another class (base or parent).  
- Promotes code reusability and hierarchical classification.

### 8.2 Syntax
```csharp
public class BaseClass
{
    public void BaseMethod()
    {
        Console.WriteLine("Base method");
    }
}

public class DerivedClass : BaseClass
{
    public void DerivedMethod()
    {
        Console.WriteLine("Derived method");
    }
}

// Usage
DerivedClass d = new DerivedClass();
d.BaseMethod();     // From BaseClass
d.DerivedMethod();  // From DerivedClass
```

### 8.3 Types of Inheritance
- **Single Inheritance**: One base class, one derived class (as shown above).
- **Multilevel Inheritance**: A derived class is also a base class for another class.
- **Hierarchical Inheritance**: Multiple derived classes from the same base class.

*(Multiple inheritance of classes is not supported in C#, but multiple interface implementation is allowed.)*

---

## 9. Exception Handling

### 9.1 What is Exception Handling?
- A mechanism to handle runtime errors or exceptional conditions in a controlled manner.

### 9.2 Keywords
1. **try**: Wrap code that might throw an exception.
2. **catch**: Handles an exception if thrown in the `try` block.
3. **finally**: A block that always executes, regardless of whether an exception is thrown or not.
4. **throw**: Used to explicitly throw an exception.

> **Note**: In C#, we do not use `throws` in method signatures like Java does; we only use `throw`.

### 9.3 Basic Structure
```csharp
try
{
    // Code that might throw an exception
    int x = int.Parse("not a number"); // This will throw FormatException
}
catch (FormatException ex)
{
    Console.WriteLine("Format exception occurred: " + ex.Message);
}
catch (Exception ex)
{
    Console.WriteLine("Some other exception occurred: " + ex.Message);
}
finally
{
    Console.WriteLine("This always executes.");
}
```

### 9.4 Custom Exceptions
- You can create your own exception by inheriting from `System.Exception`.
```csharp
public class MyCustomException : Exception
{
    public MyCustomException(string message) : base(message) { }
}
```

---

## 10. Threading

### 10.1 What is Threading?
- **Threading** allows multiple tasks to run concurrently within a single application.  
- A **thread** is a path of execution in a program.

### 10.2 Creating a Thread
```csharp
using System.Threading;

Thread t = new Thread(SomeMethod);
t.Start();

void SomeMethod()
{
    Console.WriteLine("Thread started");
}
```

### 10.3 Thread Lifecycle
1. **Unstarted**: The thread is created but not started.
2. **Running**: After calling `Start()`, the thread begins execution.
3. **Blocked/Waiting**: The thread is blocked (e.g., waiting for I/O or a lock).
4. **Stopped**: The thread has completed execution or been terminated.

### 10.4 Multithreaded Program Example
```csharp
Thread t1 = new Thread(Method1);
Thread t2 = new Thread(Method2);
t1.Start();
t2.Start();

void Method1()
{
    for (int i = 0; i < 5; i++)
    {
        Console.WriteLine("Method1 is running");
        Thread.Sleep(500);
    }
}

void Method2()
{
    for (int i = 0; i < 5; i++)
    {
        Console.WriteLine("Method2 is running");
        Thread.Sleep(500);
    }
}
```
- Threads `t1` and `t2` run concurrently.

---

## 11. File I/O

### 11.1 Overview
- **File I/O** in C# is typically done through the `System.IO` namespace.
- Common classes:
  - `FileStream`
  - `StreamReader`
  - `StreamWriter`
  - `BinaryReader`
  - `BinaryWriter`

### 11.2 FileStream
- Low-level I/O for reading/writing bytes to a file.
```csharp
using (FileStream fs = new FileStream("example.txt", FileMode.OpenOrCreate))
{
    // Read or write bytes directly
    fs.WriteByte(65); // Writes ASCII 'A'
}
```

### 11.3 StreamReader and StreamWriter
- Higher-level text-based I/O.
```csharp
// Writing text to a file
using (StreamWriter writer = new StreamWriter("example.txt"))
{
    writer.WriteLine("Hello World");
}

// Reading text from a file
using (StreamReader reader = new StreamReader("example.txt"))
{
    string content = reader.ReadToEnd();
    Console.WriteLine(content);
}
```

### 11.4 BinaryReader and BinaryWriter
- Used for reading and writing primitive data types as binary.
```csharp
// Writing binary data
using (BinaryWriter writer = new BinaryWriter(File.Open("data.bin", FileMode.Create)))
{
    writer.Write(123);      // int
    writer.Write(true);     // bool
    writer.Write("Hello");  // string
}

// Reading binary data
using (BinaryReader reader = new BinaryReader(File.Open("data.bin", FileMode.Open)))
{
    int number = reader.ReadInt32();
    bool flag = reader.ReadBoolean();
    string text = reader.ReadString();
}
```

---

## 12. Serialization

### 12.1 What is Serialization?
- **Serialization** is the process of converting an object into a format that can be stored or transmitted (e.g., binary, XML, JSON).  
- **Deserialization** is the reverse process: converting stored/transmitted data back into an object.

### 12.2 Why Use Serialization?
- To save object state to a file or database.
- To send objects over a network.

### 12.3 Binary Serialization Example (Obsolete in .NET 5+ but still conceptually useful)
```csharp
[Serializable]
public class Employee
{
    public int Id { get; set; }
    public string Name { get; set; }
}

// Serialization
using (FileStream fs = new FileStream("employee.dat", FileMode.Create))
{
    BinaryFormatter formatter = new BinaryFormatter();
    Employee emp = new Employee { Id = 1, Name = "Bob" };
    formatter.Serialize(fs, emp);
}

// Deserialization
using (FileStream fs = new FileStream("employee.dat", FileMode.Open))
{
    BinaryFormatter formatter = new BinaryFormatter();
    Employee deserializedEmp = (Employee)formatter.Deserialize(fs);
    Console.WriteLine($"Id: {deserializedEmp.Id}, Name: {deserializedEmp.Name}");
}
```
> **Note**: In modern .NET versions, `BinaryFormatter` is considered insecure. Consider using other formats like JSON or XML with `System.Text.Json` or `XmlSerializer`.

### 12.4 JSON Serialization Example (Preferred in modern .NET)
```csharp
using System.Text.Json;

public class Employee
{
    public int Id { get; set; }
    public string Name { get; set; }
}

// Serialization to JSON
Employee emp = new Employee { Id = 1, Name = "Bob" };
string jsonString = JsonSerializer.Serialize(emp);

// Deserialization from JSON
Employee deserialized = JsonSerializer.Deserialize<Employee>(jsonString);
Console.WriteLine(deserialized.Name);
```

---

## Summary

1. **.NET Architecture**: Provides a runtime (CLR) and a set of libraries, enabling cross-language interoperability and standardized type definitions (CTS, CLS).  
2. **Classes and Objects**: The core building blocks of C#. Classes define structure; objects are instances in memory.  
3. **Interfaces**: Contracts that define methods/properties without implementations. Classes must implement them fully.  
4. **Access Modifiers**: Control visibility (public, private, protected, internal, etc.).  
5. **Arrays**: Fixed-size collections for storing elements of the same type.  
6. **Inheritance**: Mechanism to reuse and extend code. C# supports single class inheritance and multiple interface implementation.  
7. **Exception Handling**: Using try/catch/finally/throw to manage runtime errors.  
8. **Threading**: Enables concurrent operations. Managed through classes like `Thread` and higher-level abstractions (Tasks, async/await in advanced scenarios).  
9. **File I/O**: Reading/writing data using streams (`FileStream`, `StreamReader`, `StreamWriter`, etc.).  
10. **Serialization**: Converting objects to/from a storable or transmittable format (binary, XML, JSON, etc.).


---
