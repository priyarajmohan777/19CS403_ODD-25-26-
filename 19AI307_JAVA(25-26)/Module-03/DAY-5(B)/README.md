# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program that uses the Boolean wrapper class in conditional logic to determine a pass/fail result.

## For example:
<img width="321" height="114" alt="image" src="https://github.com/user-attachments/assets/9bdd7de7-aec2-466a-a0ee-cf8d3f4a8ea5" />


## AIM:
To write a Java program that uses the Boolean wrapper class in conditional logic to determine whether a student has passed or failed.

## ALGORITHM :
1.	Start the program.
2.	Import the package java.util to read input from the user.
3.	Read the marks of the student as an integer using Scanner.
4.	Create a Boolean wrapper object isPass and assign the condition marks >= 50 to it.
5.	Use an if statement to check the value of isPass.
6.	If true, print "Result: Pass"; otherwise print "Result: Fail".
7.	Close the scanner object.
8.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: PRIYA R
RegisterNumber: 212222040124
*/
```

## SOURCE CODE:

```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();

        Boolean isPass = marks >= 50; 

        if (isPass) {
            System.out.println("Result: Pass");
        } else {
            System.out.println("Result: Fail");
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="417" height="239" alt="image" src="https://github.com/user-attachments/assets/bc77362d-99a8-4d2e-8b5b-978a6a70b6f7" />

## RESULT:
Thus, the Java program using the Boolean wrapper class to determine pass or fail status is implemented successfully.
