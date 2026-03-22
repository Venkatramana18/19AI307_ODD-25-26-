# Ex.No:2(B) METHODS

## QUESTION:

Write a Java program with instance method calculateSum() that sums elements of an integer array. Class name is ArrayOps. Return type is int.

## AIM:

To write a Java program to calculate the sum of elements in an integer array using the calculateSum() method in the ArrayOps class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of elements n from the user using Scanner.
4. Create an integer array of size n and read the array elements from the user.
5. Call the method calculateSum() and pass the array as an argument to compute the sum of all elements.
6. Display the calculated sum and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.*;
public class ArrayOps {

    public static int calculateSum(int [] arr) {
        int sum = 0;
        for(int i:arr){
            sum+=i;
        }
        return sum;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int arr[] = new int[n];
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        int result = calculateSum(arr);
        System.out.println(result);
    }
}
```





## OUTPUT:

<img width="486" height="198" alt="image" src="https://github.com/user-attachments/assets/d8b8503f-5caf-4125-8810-2dac7f249976" />

## RESULT:

The Java program was executed successfully, and the sum of the elements in the given integer array was calculated and displayed as output.
