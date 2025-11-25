# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a java program using class to perform addition of two numbers using parameterised constructor.

### For example:
<img width="417" height="135" alt="image" src="https://github.com/user-attachments/assets/3b1fe455-331b-478b-b713-2ad0c6a941d5" />


## AIM:
To write a Java program to perform the addition of two numbers using a class with a parameterized constructor.

## ALGORITHM :
1. Start the program.

2. Import the package java.util to read input values.

3. Create a class prog and define a parameterized constructor that accepts two integer parameters.

4. Inside the constructor, calculate the sum of the two numbers and print the result.

5. In the main() method, create a Scanner object to take two integer inputs from the user.

6. Create an object of the class prog and pass the input values to the parameterized constructor.

7. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: PRIYA R
RegisterNumber: 212222040124 
*/
```

## SOURCE CODE:

```
import java.util.*;
public class prog
{
    prog(int n1,int n2)
    {
        System.out.println("Sum = " + (n1+n2));
    }
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();
        prog p = new prog(num1,num2);
    }
}
```

## OUTPUT:
<img width="357" height="294" alt="image" src="https://github.com/user-attachments/assets/b6eaed60-0f8f-493b-966a-20fa424c4ddd" />

## RESULT:
Thus, the Java program to perform addition using a parameterized constructor is implemented successfully.
