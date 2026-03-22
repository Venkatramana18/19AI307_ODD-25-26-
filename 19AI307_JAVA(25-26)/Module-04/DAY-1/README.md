# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To write a Java program that checks whether an Integer object is null before calling its toString() method, and prevent a NullPointerException by displaying a proper message when the object is null.

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read an integer value from the user.
4. Declare an Integer object and initialize it to null.
5. If the user-entered number is not zero, assign that number to the Integer object.
6. Check whether the Integer object is not null.
7. If it is not null, print the value using toString().
8. Otherwise, print "Null Integer".
9. End the program.
    
## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        Integer obj = null;
        if (num != 0) {
            obj = num;
        }
        if (obj != null) {
            System.out.println(obj.toString());
        } else {
            System.out.println("Null Integer");
        }
    }
}
```

## OUTPUT:

<img width="436" height="261" alt="image" src="https://github.com/user-attachments/assets/3fa8dcfc-dee5-4aef-9f6d-b681c5fcfb8a" />

## RESULT:
Thus, the program successfully checks whether an Integer object is null before calling the toString() method.


