# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.
The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.
Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

Hidden Clue:
Use Singleton to manage shared access.
Count and log each print job submission.
Validate that state is preserved across all accesses.

### For example:
<img width="580" height="166" alt="image" src="https://github.com/user-attachments/assets/3708147c-1d2a-4c3b-b488-e0e91e2b73d6" />


## AIM:
To write a Java program that implements a Singleton-based Print Spooler Manager to manage shared print jobs while preserving a single instance across the system.

## ALGORITHM :
1.	Start the program.
2.	Import the java.util package for input.
3.	Create the class PrintSpoolerManager with a private static instance and a private constructor.
4.	Create the getInstance() method to return the same single instance.
5.	Create the submitJob() method to increment job count.
6.	In main(), read the number of job submissions and department names.
7.	For each job, call getInstance() and submitJob() and print the result.
8.	Stop the program.
   
## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: PRIYA R
RegisterNumber: 212222040124 
*/
```

## SOURCE CODE:
```
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance = null;
    private int jobCount = 0;

    private PrintSpoolerManager() {}

    public static PrintSpoolerManager getInstance() {
        if (instance == null) {
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

        sc.close();
    }
}
```

## OUTPUT:
<img width="1184" height="434" alt="image" src="https://github.com/user-attachments/assets/56dbbbdc-37de-4591-a9b2-fbc51fd7c086" />

## RESULT:
Thus, the Java program implementing a Singleton-based print spooler manager to manage shared print jobs is implemented successfully.
