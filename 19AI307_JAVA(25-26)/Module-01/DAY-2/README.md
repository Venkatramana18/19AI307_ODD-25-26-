# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it says "Skipped".

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.

## AIM:

To write a Java program to simulate a magical elevator that prints different messages based on the floor number using conditional statements.

## ALGORITHM :
1.	Start the program.
2.	Read the floor number from the user.
3. Check if the number is divisible by both 3 and 5; if yes, print "Skipped".
4. Else if the number is divisible by 3, print "Beware!"; if divisible by 5, print "Blessings!".
5. Otherwise print "Floor {number}" and stop the program.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
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
        int x=sc.nextInt();
        if((x%3==0)&&(x%5==0))
        {
            System.out.println("Skipped");
        }
        else if (x%3==0)
        {
            System.out.println("Beware!");
        }
        else if (x%5==0)
        {
            System.out.println("Blessings!");
        }
        else
        {
            System.out.println("Floor "+x);
        }
    }
}
```






## OUTPUT:

<img width="600" height="238" alt="image" src="https://github.com/user-attachments/assets/28e12781-cb17-472c-a91e-e24103eb871c" />


## RESULT:

The program executed successfully and printed the correct elevator message based on the floor number.
