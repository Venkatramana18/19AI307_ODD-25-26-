# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

Marks ≥ 90: Grade A

Marks ≥ 75 and < 90: Grade B

Marks ≥ 50 and < 75: Grade C

Marks < 50: Grade F

## AIM:

To write a Java program to create a superclass Person with fields name and age, and a subclass Student that inherits from Person and calculates the grade based on marks.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a superclass Person with variables name and age, and initialize them using a constructor.
4. Create a subclass Student that inherits from Person and adds a variable marks.
5. Create a constructor in Student to initialize name, age, and marks using the super keyword.
6. Implement the method calculateGrade() to return grade A, B, C, or F based on the marks condition.
7. In the main method, read the student details, create a Student object, display the details, and print the calculated grade.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.*;
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

class Student extends Person {
    int marks;

    Student(String name, int age, int marks) {
        super(name, age);
        this.marks = marks;
    }

    char calculateGrade() {
        if (marks >= 90)
            return 'A';
        else if (marks >= 75 && marks<90)
            return 'B';
        else if (marks >= 50&& marks<75)
            return 'C';
        else
            return 'F';
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        int age=sc.nextInt();
        int marks=sc.nextInt();
        Student s = new Student(name,age,marks);
         System.out.println("Name: "+name);
         System.out.println("Age: "+age);
         System.out.println("Marks: "+marks);
        System.out.println("Grade: "+s.calculateGrade());
    }
}
```





## OUTPUT:

<img width="842" height="590" alt="image" src="https://github.com/user-attachments/assets/63b89ae2-06aa-41e1-90ea-73ee2c2b82d6" />

## RESULT:

The Java program was executed successfully.
The Student class inherited the properties of the Person class, and the grade was calculated correctly based on the student's marks.
