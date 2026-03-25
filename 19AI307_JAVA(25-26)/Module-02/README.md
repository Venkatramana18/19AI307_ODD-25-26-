# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:

Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:

To write a Java program to create a Car class with attributes brand, model, and year, create two objects, and print their details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create a class Car with attributes brand, model, and year.
4. In the main() method, create two objects car1 and car2 of the Car class.
5. Assign values to the attributes of both objects.
6. Print the details of both cars and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296 
*/
```

## SOURCE CODE:

```

public class prog {
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
    
}
class Car{
    String brand;
    String model;
    int year;
}
```




## OUTPUT:
<img width="540" height="142" alt="image" src="https://github.com/user-attachments/assets/0009ecbc-6aaa-4c76-b622-df7c3b306df5" />


## RESULT:

The program compiled and executed successfully and displayed the details of the two car objects.

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

# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## AIM:

To write a Java program to create a class Calculator with a non-static method add(int a, int b) to return the sum of two numbers and a static method info() to display a message.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Calculator.
4. Define a non-static method add(int a, int b) that returns the sum of two integers.
5. Define a static method info() that prints the message "Calculator is ready".
6. In the main method, read two integers from the user using Scanner, call the static method using the class name, and create an object of the Calculator class.
7. Call the add() method using the object, display the result, and stop the program.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Venkat Ramana S B
RegisterNumber:  212224060296
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Calculator {
   public int add(int a,int b){
       return a+b;
   }
   public static void info(){
       System.out.println("Calculator is ready");
   }
}

class prog {
    public static void main(String[] args) {
         Scanner sc=new Scanner(System.in);
         int n=sc.nextInt();
         int m=sc.nextInt();
         Calculator.info();
         Calculator obj=new Calculator();
         System.out.println("Sum: "+obj.add(n,m));
    }
}
```





## OUTPUT:

<img width="655" height="324" alt="image" src="https://github.com/user-attachments/assets/774bb2c5-23a0-44b7-b2e7-e6d48ad6a355" />

## RESULT:

The Java program was executed successfully.
The static method info() displayed the message "Calculator is ready", and the non-static method add() calculated and displayed the sum of the two input numbers.

