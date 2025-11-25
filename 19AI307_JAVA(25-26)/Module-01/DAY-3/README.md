# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Check if the number is Armstrong or not.

### For example:

<img width="367" height="84" alt="image" src="https://github.com/user-attachments/assets/d9510e9d-cbd8-4395-8929-6c42f37ea78b" />

## AIM:
To write a Java program to check whether a given number is an Armstrong number using looping statements.

## ALGORITHM :

1. Start the program.

2. Import the package java.util and create a Scanner object to read the input number.

3. Read the integer input from the user and store the original number.

4. Use a while loop to count the total number of digits in the given number.

5. Initialize sum = 0 and again use a while loop to extract each digit of the number.

6. For each digit, use a for loop to compute the digit raised to the power of the total number of digits and add it to sum.

7 Compare the calculated sum with the original number; if they are equal, print that it is an Armstrong number, otherwise print that it is not.

8. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: PRIYA R
RegisterNumber:  212222040124
*/
```

## SOURCE CODE:

```
import java.util.*;
public class Armstrong {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int org = num;

        int digits = 0, temp = num;
        while (temp > 0) {
            digits++;
            temp /= 10;
        }


        int sum = 0;
        temp = num;
        while (temp > 0) {
            int digit = temp % 10;
            int power = 1;
            for (int i = 0; i < digits; i++) {
                power *= digit;   
            }
            sum += power;
            temp /= 10;
        }

        if (sum == org)
            System.out.println(org + " is an Armstrong number.");
        else
            System.out.println(org + " is not an Armstrong number.");
    }
}
```

## OUTPUT:

<img width="780" height="234" alt="image" src="https://github.com/user-attachments/assets/07910fe4-59f7-4d1d-a706-e5179dee1b3f" />


## RESULT:
Thus, the Java program to determine whether a number is an Armstrong number using looping statements is executed successfully.
