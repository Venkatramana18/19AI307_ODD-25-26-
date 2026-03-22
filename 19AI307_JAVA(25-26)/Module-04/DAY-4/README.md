# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

## AIM:
To implement the Factory Design Pattern to send different types of notifications — Email, SMS, and Push.

## ALGORITHM :
1.	Create a Notification interface with the method notifyUser().
2.	Implement this interface in classes EmailNotification, SMSNotification, and PushNotification.
3.	Create a NotificationFactory class to generate objects based on input type.
4.	In main(), read the notification type and get the corresponding object from the factory.
5.	Call the notifyUser() method to send the notification.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface Notification {
    void notifyUser();
}
class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}
class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}
class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}
class NotificationFactory {
    public Notification createNotification(String type) {
        switch(type.toLowerCase()) {
            case "email": return new EmailNotification();
            case "sms": return new SMSNotification();
            case "push": return new PushNotification();
            default: return null;
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        NotificationFactory factory = new NotificationFactory();
        while(true) {
            String input = sc.nextLine();
            if(input.equalsIgnoreCase("exit")) break;
            Notification notification = factory.createNotification(input);
            if(notification != null) {
                notification.notifyUser();
            } else {
                System.out.println("Invalid notification type: " + input);
            }
        }
    }
}

```

## OUTPUT:

<img width="608" height="268" alt="image" src="https://github.com/user-attachments/assets/76d9ccaa-8948-4dde-a0d8-8c1dbea34ac5" />

## RESULT:
Thus, the program successfully creates and sends the appropriate type of notification using the Factory Pattern.

