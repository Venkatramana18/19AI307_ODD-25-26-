# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:

To write a Java program to create a class Smartphone with private instance variables brand, model, and storageCapacity, provide getter and setter methods, and implement a method increaseStorage() to increase the storage capacity.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Smartphone with private variables brand, model, and storageCapacity.
4. Provide public getter and setter methods to access and modify these variables.
5. Define a method increaseStorage(int value) to increase the storage capacity if the value is greater than 0.
6. In the main method, create an object of the Smartphone class and read the brand, model, storage capacity, and additional storage value from the user.
7. Call the increaseStorage() method, display the updated smartphone details, and end the program.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    
    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    
    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

   
    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    
    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}
//type your code here
public class lulu{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        Smartphone s=new Smartphone();
        s.setBrand(sc.nextLine());
        s.setModel(sc.nextLine());
        s.setStorageCapacity(sc.nextInt());
        s.increaseStorage(sc.nextInt());
        s.display();
    }
}
```





## OUTPUT:

<img width="964" height="472" alt="image" src="https://github.com/user-attachments/assets/03546812-83c9-4ef4-ae6a-aa458b089b8a" />

## RESULT:

The Java program was executed successfully.
The Smartphone class variables were accessed and modified using getter and setter methods, and the storage capacity was increased using the increaseStorage() method and displayed correctly.
