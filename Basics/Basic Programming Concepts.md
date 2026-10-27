# Parameters vs. Arguments

```java
public int Add(int a, int b)
{
    return a + b;
}
```

Here, a and b are parameters. They are placeholders defined by the method.

When calling it:

```java
Add(10, 20);
```

10 and 20 are arguments. They are the actual values passed to the method.

- Parameters = Values a method expects.
- Arguments = Values you provide when calling it.



# What is a Class?

A class is a blueprint or template for creating objects

Imagine a university with thousands of students.

Every student has certain information:
- Name
- Age
- Roll number
- GPA
Every student may also perform actions:
- Study
- Enroll in a course
- Submit assignments
Instead of writing separate code for each student, you create a class describing what all students have in common.

```java
public class Student
{
    public string Name { get; set; } = "";
    public int Age { get; set; }
    public double GPA { get; set; }

    public void Study()
    {
        Console.WriteLine("Student is studying");
    }
}
```
- Here, Student is a class.
- Name, Age, and GPA are properties.
- Study() is a method.

The class defines the structure, but each student object stores its own values.


# What is an Object?

An object is an actual instance of a class.

For example:
```java
Student student1 = new Student();

student1.Name = "Ahmed";
student1.Age = 20;
student1.GPA = 3.5;
```

- Student (Left side): The data type or class name. It acts as a blueprint.
- student1: The reference variable (not the object itself). It stores the memory address pointing to where the object lives.
- new: The keyword used to allocate memory in the heap for the new object.
- Student(): The constructor method called to initialize the object.


You can create another student:

```java
Student student2 = new Student();

student2.Name = "Ali";
student2.Age = 22;
student2.GPA = 3.8;
```


# What is an Instance?

an object and an instance are largely the same thing, and the terms are often used interchangeably. However, they differ slightly in the context and relationship they emphasize.

The primary difference lies in how you view the entity:
• Object is the generic, independent entity. It represents a concrete "thing" created in memory that bundles data (attributes) and behavior (methods) together.
• Instance is a term used to highlight the relationship between that object and its blueprint (the class). It emphasizes that the object is a specific "example" or realization of that class.

```java
Student student = new Student();
```
The variable student refers to an instance of the Student class.

# What does new mean?

The new keyword creates an instance of a class.
```java
Student student = new Student();
```

# What is a Constructor?
A constructor is a special member that runs when an object is created.

Its purpose is to initialize the object.

Think of it as the "setup crew" for your object. Its primary purpose is to initialize the object’s initial state by assigning values to its data fields and performing any required setup logic.
Basically It is a foundational tool used across languages to guarantee that objects start their life cycle in a predictable, valid state.

```java
public class Student
{
    public string Name { get; set; }
    public int Age { get; set; }

    public Student(string name, int age)
    {
        Name = name;
        Age = age;
    }
}
```

Now you can create a student and provide its information immediately:

```java 
Student student = new Student("Ahmed", 20);
```


The constructor assigns the provided values.

Notice that the constructor has the same name as the class and does not declare a return type.

# What is a Property?

A property provides controlled access to a value associated with an object.

For example:
```java
public string Name { get; set; } = "";
```

Key Components: Accessors (get and set)

Properties use accessors to control how data is handled:
Here:
- get — Allows the value to be read.
- set — Allows the value to be changed.
Usage:

```java
student.Name = "Ahmed";         // Setter
Console.WriteLine(student.Name); // Getter
```

Properties can also contain validation or calculations.

# What is a Field? 

A field is a variable declared directly inside a class or struct.

```java
public class Student
{
    private string name = "";
}
```

Here, name is a field.

Now compare it with a property:

```java
public class Student
{
    private string name = "";

    public string Name
    {
        get { return name; }
        set { name = value; }
    }
}
```

name is a private field, while Name is a public property that controls access to the field.

In modern C#, auto-properties such as public string Name { get; set; } are very common.


# What is a Method?

A method is an operation associated with a class or object.

```java
public class Calculator
{
    public int Multiply(int a, int b)
    {
        return a * b;
    }
}
```


Using it:

```java
Calculator calc = new Calculator();

int answer = calc.Multiply(5, 10);
Console.WriteLine(answer); // 50
```


A method defines what an object can do.

A property represents information about an object.


# What is this?

The this keyword refers to the current object.

For example:

```java
public class Student
{
    public string Name { get; set; }

    public Student(string name)
    {
        this.Name = name;
    }
}
```

this.Name means the Name property belonging to the current object.

It becomes particularly useful when parameter and field names are the same:

```java
private string name;

public Student(string name)
{
    this.name = name;
}
```

Here, this.name refers to the field, while name refers to the constructor parameter.

# What is static?

the static keyword means that a member (a variable, method, property, or constructor) or a class belongs to the type itself rather than to a specific instance (object) of that type

Example:
```java
public class Calculator
{
    public static int Add(int a, int b)
    {
        return a + b;
    }
}
```

You can call it without creating a Calculator object:
```java
int result = Calculator.Add(10, 20);
```

Compare:
```java
// Instance method
Calculator calc = new Calculator();
calc.Multiply(5, 10);

// Static method
Calculator.Add(5, 10);
```

Static members are useful for operations that do not require individual object state.