# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You are writing a Java program where you read a string input. If the input is "init", you create an object and call its method. If it's "null", no object is created.
Your program crashes with a NullPointerException when "null" is entered.
What caused the crash and how can you handle it to prevent the error?

### For example:
<img width="202" height="124" alt="image" src="https://github.com/user-attachments/assets/e8b6d260-623e-4337-be17-6a8a0e4e9ff3" />


## AIM:
To write a Java program that demonstrates exception handling by catching a NullPointerException when an object is not initialized based on user input.

## ALGORITHM :
1.	Start the program.
2.	Import the package java.util to accept user input.
3.	Create a class Example with a method display() that prints a message.
4.	In the main() method, read a string input from the user.
5.	Declare an object reference of type Example and initialize it to null.
6.	If the input is "init", create an object; otherwise, leave the object reference as null.
7.	Surround the method call obj.display() with a try block.
8.	Catch the NullPointerException using a catch block and print an appropriate message.
9.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: PRIYA R
RegisterNumber: 212222040124 
*/
```

## SOURCE CODE:
```
import java.util.*;

class Example
{
    void display()
    {
        System.out.println("Object exists");
    }
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String input = sc.next();
        
        Example obj = null;
      if(input.equalsIgnoreCase("init"))
      {
          obj = new Example();
      }
        
        
        try
        {
            obj.display();
        }
        catch(NullPointerException e)
        {
            System.out.println("Object is null");
        }
    }
}
```

## OUTPUT:

<img width="509" height="232" alt="image" src="https://github.com/user-attachments/assets/71a54d6a-094d-43a2-a609-66d71656f44b" />


## RESULT:
Thus, the Java program demonstrating exception handling using a try-catch block to prevent a NullPointerException is implemented successfully.
