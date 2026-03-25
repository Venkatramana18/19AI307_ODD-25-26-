# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To write a Java program that checks whether an Integer object is null before calling its toString() method, and prevent a NullPointerException by displaying a proper message when the object is null.

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read an integer value from the user.
4. Declare an Integer object and initialize it to null.
5. If the user-entered number is not zero, assign that number to the Integer object.
6. Check whether the Integer object is not null.
7. If it is not null, print the value using toString().
8. Otherwise, print "Null Integer".
9. End the program.
    
## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        Integer obj = null;
        if (num != 0) {
            obj = num;
        }
        if (obj != null) {
            System.out.println(obj.toString());
        } else {
            System.out.println("Null Integer");
        }
    }
}
```

## OUTPUT:

<img width="436" height="261" alt="image" src="https://github.com/user-attachments/assets/3fa8dcfc-dee5-4aef-9f6d-b681c5fcfb8a" />

## RESULT:
Thus, the program successfully checks whether an Integer object is null before calling the toString() method.


# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.
The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.
Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

## AIM:
To implement a Java program that simulates a centralized print job manager using the Singleton Design Pattern, where multiple departments send print jobs and the manager keeps track of the total number of jobs in the queue.

## ALGORITHM :
1. Start the program.
2. Create a Singleton class PrintSpoolerManager that ensures only one print manager object exists.
3. Inside the class, maintain a counter to track the total print jobs.
4. Provide a method getInstance() to return the same object each time it is called.
5. Provide another method submitJob(department) which:
   
       Displays which department submitted the job.
   
       Increments the total print job counter.

       Prints the updated job count.
7. In the main() method:
      ```
      Read the number of print job requests from the user.
      
      For each job, read the department name.

      Call submitJob() using the Singleton manager instance.
      ```
8. Display the print job submission message for each department.
9. End the program.
   
## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296
*/
```

## SOURCE CODE:
```
import java.util.*;
class PrintSpoolerManager {
    private static PrintSpoolerManager instance;
    private int jobCount = 0;
    private PrintSpoolerManager(){}
    public static PrintSpoolerManager getInstance() {
        if(instance == null){
            instance = new PrintSpoolerManager();
        }
        return instance;
    }
    public int submitJob(String department) {
      jobCount++;
      return jobCount;
    }
}
public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```

## OUTPUT:

<img width="1118" height="369" alt="image" src="https://github.com/user-attachments/assets/05b6185f-b57e-493f-acc9-e66f6a0d7254" />

## RESULT:
Thus, the program successfully simulates a centralized print manager, Each department submits a print job, and the Singleton manager updates the job count after every submission.

# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## AIM:
To demonstrate the Abstract Factory Pattern by creating families of related objects (Herbivore and Carnivore) from two regions — Africa and Asia.

## ALGORITHM :
1.	Define interfaces for Herbivore and Carnivore.
2.	Create concrete classes for African (Zebra, Lion) and Asian (Deer, Tiger) animals.
3.	Define an AnimalFactory interface with methods to create herbivores and carnivores.
4.	Implement concrete factories: AfricaAnimalFactory and AsiaAnimalFactory.
5.	In main(), use factories to create animals and simulate interactions.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}
class Wildebeest implements Herbivore {}
class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}
class Buffalo implements Herbivore {}
class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}
interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}
class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Wildebeest(); }
    public Carnivore createCarnivore() { return new Lion(); }
}
class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Buffalo(); }
    public Carnivore createCarnivore() { return new Tiger(); }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;
        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }
        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}
```

## OUTPUT:

<img width="565" height="230" alt="image" src="https://github.com/user-attachments/assets/c7343a74-d599-411f-935d-b545b0da21b7" />

## RESULT:
Thus, the program successfully demonstrates the Abstract Factory Pattern, showing different animal interactions for Africa and Asia.


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

# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento Design Pattern that allows saving and restoring versions of an Article object.

## ALGORITHM :
1.	Create ArticleMemento to store article content (state).
2.	Create Article (Originator) that can write, save, and restore content.
3.	Create VersionHistory (Caretaker) to store multiple mementos.
4.	Allow the user to:
5.	Write new content
6.	Save current version
7.	View all saved versions
8.	Restore any version
9.	Display restored version content.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Venkat Ramana S B
RegisterNumber: 212224060296
*/
```

## SOURCE CODE:
```
import java.util.*;
class Article {
    private String content;
    public Article(String content) {
        this.content = content;
    }
    public void setContent(String content) {
        this.content = content;
    }
    public String getContent() {
        return content;
    }
    public ArticleMemento save() {
        return new ArticleMemento(content);
    }
    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}
class ArticleMemento {
    private final String content;
    public ArticleMemento(String content) {
        this.content = content;
    }
    public String getContent() {
        return content;
    }
}
class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();
    public void saveVersion(Article article) {
        versions.add(article.save());
    }
    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
    public List<ArticleMemento> getAllVersions() {
        return versions;
    }
}
public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());
        ArticleHistory history = new ArticleHistory();
        Article article = new Article("");
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }
        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento memento = history.getVersion(restoreIndex);
        if (memento != null) {
            article.restore(memento);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }
    }
}
```

## OUTPUT:

<img width="656" height="467" alt="image" src="https://github.com/user-attachments/assets/4ff429ff-9c4d-44d8-be03-44ff22fefc07" />

## RESULT:
Thus, the program successfully demonstrates the Memento Pattern, allowing the user to save, view, and restore different versions of an article.



