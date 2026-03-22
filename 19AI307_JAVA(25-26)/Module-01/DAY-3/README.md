# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

In mathematics, the factorial of a non-negative integer n, denoted as n!, is the product of all positive integers less than or equal to n. For example:

5! = 5 × 4 × 3 × 2 × 1 = 120

3! = 3 × 2 × 1 = 6

0! is defined as 1.

Write a Java program that prompts the user to enter a non-negative integer and then calculates and displays the factorial of the given number.

Use a for loop to perform the calculation.

Make sure to handle the case when the user enters 0.

Display the result in a clear and user-friendly way.

## AIM:

To write a Java program to find the factorial of a given non-negative integer using a for loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a non-negative integer n from the user using Scanner.
4. If n = 0, print "Factorial of 0 is: 1".
5. Otherwise, use a for loop from 1 to n and multiply the numbers to calculate the factorial.
6. Display the factorial result and end the program.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
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
        int n=sc.nextInt();
        int f=1;
        
        if(n==0){
            System.out.println("Factorial of 0 is: 1");
        }
        else{
             for(int i=1;i<=n;i++){
                 f=f*i;
             }
             System.out.println("Factorial of "+n+" is: "+f);
        }
        
    }
}

```




## OUTPUT:

<img width="723" height="201" alt="image" src="https://github.com/user-attachments/assets/836b4a28-cf0a-4e11-9d6c-0ea6fa0169af" />


## RESULT:

The program executed successfully and displayed the factorial of the entered number.
