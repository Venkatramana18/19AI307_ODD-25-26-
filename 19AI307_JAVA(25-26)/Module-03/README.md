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

# Ex.No:3(b) POLYMORPHISM

## QUESTION:

Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:

area(int side) for square

area(int length, int breadth) for rectangle

area(double radius) for circle

## AIM:

To write a Java program to calculate the area of different shapes using method overloading in the class AreaCalculator.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class AreaCalculator.
4. Define three overloaded methods named area():
5. area(int side) to calculate the area of a square.
6. area(int length, int breadth) to calculate the area of a rectangle.
7. area(double radius) to calculate the area of a circle.
8. In the main method, create a Scanner object to read input values for side, length, breadth, and radius.
9. Create an object of the AreaCalculator class and call the overloaded area() methods with the respective parameters.
10. Display the calculated areas for the square, rectangle, and circle and end the program.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.*;
class AreaCalculator{
    int area(int s){
        return s*s;
        
    }
    int area(int l,int b){
        return l*b;
    }
    double area(double r){
        return Math.PI*r*r;
    }
}
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int s=sc.nextInt();
        int l=sc.nextInt();
        int b=sc.nextInt();
        double r=sc.nextDouble();
        AreaCalculator a=new AreaCalculator();
        System.out.println("Area of square: "+a.area(s));
        System.out.println("Area of rectangle: "+a.area(l,b));
        System.out.println("Area of circle: "+a.area(r));
    }
}
```





## OUTPUT:

<img width="886" height="400" alt="image" src="https://github.com/user-attachments/assets/6a435613-ab3d-47c4-b324-de39ec26b8fb" />

## RESULT:

The Java program was executed successfully, and the areas of the square, rectangle, and circle were calculated and displayed using method overloading.

# Ex.No:3(C) ABSTRACTION

## QUESTION:

Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.

## AIM:

To write a Java program using abstraction by creating an abstract class BankAccount with the method calculateInterest() and implementing it in SavingsAccount and FixedDepositAccount classes.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class BankAccount with an abstract method calculateInterest().
4. Create a subclass SavingsAccount that extends BankAccount, store the balance, and implement calculateInterest() to calculate interest at 4%.
5. Create another subclass FixedDepositAccount that extends BankAccount, store the amount and years, and implement calculateInterest() to calculate interest at 7% per year.
6. In the main method, read the account type and required inputs using Scanner, then create the appropriate object.
7. Call the calculateInterest() method using the object and display the calculated interest.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.*;

abstract class BankAccount {
    abstract double calculateInterest();
}

class SavingsAccount extends BankAccount {
    double balance;

    SavingsAccount(double balance) {
        this.balance = balance;
    }

    double calculateInterest() {
        return balance * 0.04;
    }
}

class FixedDepositAccount extends BankAccount {
    double amount;
    int years;

    FixedDepositAccount(double amount, int years) {
        this.amount = amount;
        this.years = years;
    }

    double calculateInterest() {
        return amount * 0.07 * years;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int type = sc.nextInt();
        BankAccount acc;

        if (type == 1) {
            double balance = sc.nextDouble();
            acc = new SavingsAccount(balance);
        } else {
            double amount = sc.nextDouble();
            int years = sc.nextInt();
            acc = new FixedDepositAccount(amount, years);
        }

        System.out.printf("%.2f", acc.calculateInterest());
    }
}
```





## OUTPUT:

<img width="549" height="377" alt="image" src="https://github.com/user-attachments/assets/9e59165a-69e6-4c7c-9689-792a11c0b3ab" />

## RESULT:

The Java program was executed successfully.
The abstract method calculateInterest() was implemented in both SavingsAccount and FixedDepositAccount classes, and the correct interest value was calculated and displayed based on the account type.

# Ex.No:3(D)    INTERFACE 

## QUESTION:

You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".


## AIM:

To write a Java program that uses an interface WeatherBot to predict weather conditions using different bot classes SunBot and RainBo

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface WeatherBot with a method predict(int temperature).
4. Create a class SunBot that implements WeatherBot and returns "HOT" if temperature > 30, otherwise "MODERATE".
5. Create another class RainBot that implements WeatherBot and returns "COLD" if temperature < 20, otherwise "WARM".
6. In the main method, read the temperature and bot type from the user using Scanner, and create the appropriate bot object.
7. Call the predict() method using the object and display the prediction.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface WeatherBot {
    String predict(int temperature);
}

class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30) {
            return "HOT";
        } else {
            return "MODERATE";
        }
    }
}

class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20) {
            return "COLD";
        } else {
            return "WARM";
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        WeatherBot bot;

        if (botType == 1) {
            bot = new SunBot();
        } else {
            bot = new RainBot();
        }

        System.out.println(bot.predict(temperature));
    }
}
```





## OUTPUT:

<img width="560" height="176" alt="image" src="https://github.com/user-attachments/assets/5cfb5d68-64b4-42a6-8a28-216713210ba3" />

## RESULT:

The Java program was executed successfully.
The appropriate bot (SunBot or RainBot) predicted the weather condition based on the given temperature and displayed the result.

# Ex.No:3(E) INNER CLASS

## QUESTION:

Write a Java program where the inner class is declared private and accessed through a method in the outer class.

## AIM:

To write a Java program where a private inner class is declared inside an outer class and accessed through a method of the outer class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class Outer.
4. Inside the outer class, declare a private inner class Inner with a method setData(int data) to display the value.
5. Create a method accessInner(int value) in the outer class to create an object of the inner class and call its method.
6. In the main method, read an integer input using Scanner, create an object of the Outer class, and call the accessInner() method.
7. Display the result and stop the program.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Outer {
    private class Inner {
        void setData(int data) {
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    void accessInner(int value) {
        Inner obj = new Inner();
        obj.setData(value);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        Outer outer = new Outer();
        outer.accessInner(n);
    }
}
```





## OUTPUT:

<img width="926" height="259" alt="image" src="https://github.com/user-attachments/assets/b9e5993f-1291-4dda-be07-1b0b4ee6fa57" />

## RESULT:

The Java program was executed successfully.
The private inner class was accessed through a method in the outer class, and the given data was displayed correctly.

# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:

To write a Java program to check whether a given number is an Armstrong number using Math.pow() and the Integer wrapper class.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user using Scanner and store it in an Integer wrapper variable.
4. Store the original number in another variable and initialize sum = 0.
5. Find the number of digits in the number using String.valueOf(number).length().
6. Extract each digit using the modulus operator (%), raise it to the power of the number of digits using Math.pow(), and add it to sum.
7. Compare sum with the original number. If they are equal, print that it is an Armstrong number; otherwise, print that it is not an Armstrong number.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class ArmstrongNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Integer number = sc.nextInt();
        int originalNumber = number;
        int sum = 0;

        int digits = String.valueOf(number).length();

        while (number > 0) {
            int digit = number % 10;
            sum += (int) Math.pow(digit, digits);
            number = number / 10;
        }

        if (sum == originalNumber) {
            System.out.println(originalNumber + " is an Armstrong number.");
        } else {
            System.out.println(originalNumber + " is not an Armstrong number.");
        }

        sc.close();
    }
}
```





## OUTPUT:

<img width="847" height="264" alt="image" src="https://github.com/user-attachments/assets/abaab959-3194-47c4-9e46-26100a1878a5" />

## RESULT:

The Java program was executed successfully, and the given number was checked and displayed whether it is an Armstrong number or not.
