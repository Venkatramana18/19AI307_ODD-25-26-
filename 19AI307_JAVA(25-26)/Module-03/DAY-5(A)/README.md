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
