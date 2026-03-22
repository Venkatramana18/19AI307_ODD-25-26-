# Ex.No:3(C) ABSTRACTION

## QUESTION:

Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.

## AIM:

To write a Java program using abstraction by creating an abstract class BankAccount with the method calculateInterest() and implementing it in SavingsAccount and FixedDepositAccount classes.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class BankAccount with an abstract method calculateInterest().
4. Create a subclass SavingsAccount that extends BankAccount, store the balance, and implement calculateInterest() to calculate interest at 4%.
5. Create another subclass FixedDepositAccount that extends BankAccount, store the amount and years, and implement calculateInterest() to calculate interest at 7% per year.
6. In the main method, read the account type and required inputs using Scanner, then create the appropriate object.
7. Call the calculateInterest() method using the object and display the calculated interest.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.*;

abstract class BankAccount {
    abstract double calculateInterest();
}

class SavingsAccount extends BankAccount {
    double balance;

    SavingsAccount(double balance) {
        this.balance = balance;
    }

    double calculateInterest() {
        return balance * 0.04;
    }
}

class FixedDepositAccount extends BankAccount {
    double amount;
    int years;

    FixedDepositAccount(double amount, int years) {
        this.amount = amount;
        this.years = years;
    }

    double calculateInterest() {
        return amount * 0.07 * years;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int type = sc.nextInt();
        BankAccount acc;

        if (type == 1) {
            double balance = sc.nextDouble();
            acc = new SavingsAccount(balance);
        } else {
            double amount = sc.nextDouble();
            int years = sc.nextInt();
            acc = new FixedDepositAccount(amount, years);
        }

        System.out.printf("%.2f", acc.calculateInterest());
    }
}
```





## OUTPUT:

<img width="549" height="377" alt="image" src="https://github.com/user-attachments/assets/9e59165a-69e6-4c7c-9689-792a11c0b3ab" />

## RESULT:

The Java program was executed successfully.
The abstract method calculateInterest() was implemented in both SavingsAccount and FixedDepositAccount classes, and the correct interest value was calculated and displayed based on the account type.
