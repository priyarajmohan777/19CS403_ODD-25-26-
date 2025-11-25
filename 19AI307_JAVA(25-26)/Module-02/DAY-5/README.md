# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

### For example:
<img width="256" height="116" alt="image" src="https://github.com/user-attachments/assets/01ee5804-b466-4918-bb9c-d36910fb3df5" />


## AIM:
To write a Java program to demonstrate access modifiers by using a non-static method and a static method in a class.

## ALGORITHM :
1.	Start the program.

2.	Import the java.util package to read input from the user.

3.	Create a class Calculator with a non-static method add(int a, int b) that returns the sum of two numbers.

4.	Create a static method info() that prints a message indicating readiness.

5.	In the main() method, create a Scanner object to read two integer inputs.

6.	Call the static method info() using the class name.

7.	Create an object of Calculator and call the add() method to get the sum.

8.	Print the result.

9.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: PRIYA R
RegisterNumber: 212222040124 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Calculator {
    
    int add(int a,int b)
    {
        return a+b; 
    }
    
    static void info()
    {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();
        Calculator c = new Calculator();
        Calculator.info();
        int result = c.add(num1,num2);
        System.out.println("Sum: " + result);
        
    }
}
```

## OUTPUT:
<img width="543" height="297" alt="image" src="https://github.com/user-attachments/assets/b9e769df-3bfc-4280-bc77-98f50bce91ca" />

## RESULT:
Thus, the Java program demonstrating access modifiers with static and non-static methods is implemented successfully.
