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

