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