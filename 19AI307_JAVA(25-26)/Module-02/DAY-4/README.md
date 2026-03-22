# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a program to access a static variable using both class name and object.

## AIM:

To write a Java program to access a static variable using both the class name and an object.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class StaticDemo with a static integer variable num.
4. In the main method, create a Scanner object to read input from the user.
5.Assign the input value to the static variable using the class name (StaticDemo.num).
6. Create an object of the StaticDemo class and access the static variable using the object reference (obj.num).
7. Display both outputs and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class StaticDemo {
    static int num;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        StaticDemo.num = sc.nextInt();
        
        StaticDemo obj = new StaticDemo();
        
        System.out.println("Accessing using class name: " + StaticDemo.num);
        System.out.println("Accessing using object: " + obj.num);
        
        sc.close();
    }
}
```





## OUTPUT:

<img width="841" height="328" alt="image" src="https://github.com/user-attachments/assets/b79a1348-e67a-4123-b7aa-8802a5f556fb" />

## RESULT:

The Java program was executed successfully and demonstrated that a static variable can be accessed using both the class name and the object reference, producing the same value in both cases.
