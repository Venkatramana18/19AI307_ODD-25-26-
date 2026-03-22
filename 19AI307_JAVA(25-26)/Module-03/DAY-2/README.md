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
