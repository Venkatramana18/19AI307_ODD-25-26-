# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java Program to Find the Average of Array Elements.

## AIM:

To write a Java program to find the average of elements in an array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of elements n from the user.
4. Create an array and read n elements into the array while calculating the sum of elements.
5. Compute the average using the formula:
6. Average = Sum / Number of elements.
7. Display the average of the array elements and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int[] a=new int[n];
        double sum=0;
        for(int i=0;i<n;i++){
            a[i]=sc.nextInt();
            sum+=a[i];
        }
        double avg=sum/n;
        System.out.printf("The average of elements is %.2f",avg);
    }
}
```

## OUTPUT:

![WhatsApp Image 2026-03-13 at 2 41 28 PM](https://github.com/user-attachments/assets/d205e629-4d47-4c07-85d8-61f154770777)


## RESULT:

Thus, the Java program to find the average of array elements was executed successfully and the average value was obtained for the given input.
