# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:

Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:

To write a Java program to create a Car class with attributes brand, model, and year, create two objects, and print their details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create a class Car with attributes brand, model, and year.
4. In the main() method, create two objects car1 and car2 of the Car class.
5. Assign values to the attributes of both objects.
6. Print the details of both cars and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296 
*/
```

## SOURCE CODE:

```

public class prog {
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
    
}
class Car{
    String brand;
    String model;
    int year;
}
```




## OUTPUT:
<img width="540" height="142" alt="image" src="https://github.com/user-attachments/assets/0009ecbc-6aaa-4c76-b622-df7c3b306df5" />


## RESULT:

The program compiled and executed successfully and displayed the details of the two car objects.
