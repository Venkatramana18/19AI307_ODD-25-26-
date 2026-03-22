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
