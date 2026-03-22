# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to reverse a given string.

## AIM:

To write a Java program to reverse a given string.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a string from the user using Scanner.
4. Initialize an empty string variable to store the reversed string.
5. Traverse the string from the last character to the first and add each character to the reversed string.
6. Display the reversed string and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296
*/
```

## SOURCE CODE:

```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String str=sc.nextLine();
        String rev="";
        for(int i=str.length()-1;i>=0;i--){
            rev=rev+str.charAt(i);
        }
        System.out.print("Reversed string: "+rev);
    }
}
```





## OUTPUT:

![WhatsApp Image 2026-03-13 at 2 40 53 PM](https://github.com/user-attachments/assets/11f98238-caf8-4373-94ad-22473006a471)


## RESULT:

Thus, the Java program to reverse a given string was executed successfully.
