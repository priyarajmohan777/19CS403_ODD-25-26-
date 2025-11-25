# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A train company charges tickets based on age and travel class:

Children (<12): ₹5 per km (any class)
Adults (12–60):
Sleeper: ₹10/km
AC: ₹15/km
Seniors (>60): ₹7/km (any class)

### Input format:
5
100

### Output format:
500

Task: Accept age, distance and travel class (1 for Sleeper, 2 for AC)(follow the same order to get the inputs). Calculate fare.

## AIM:

To write a Java program to calculate train ticket fare using conditional statements based on passenger age, travel class, and distance.

## ALGORITHM :

1. Start the program.

2. Import the package java.util and create a Scanner object to read inputs.

3. Read the passenger's age and distance from the user.

4. Initialize the variable fare to 0.

5. If the age is less than 12, calculate fare as ₹5 per km.

6. Else if age is between 12 and 60 (inclusive), read travel class (1 for Sleeper, 2 for AC).

7. If travel class is 1, calculate fare as ₹10 per km, otherwise if travel class is 2, calculate fare as ₹15 per km.

8. Else if age is greater than 60, calculate fare as ₹7 per km.

9. Display the calculated fare.

10. Stop the program.




## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: PRIYA R
RegisterNumber:  212222040124
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int age = sc.nextInt();
        int distance = sc.nextInt();
      
        int fare=0;
        
        if(age<12)
        fare = 5* distance;
        
        else if(age>=12 && age <=60)
        {
            int trav_class = sc.nextInt();
            if(trav_class==1)
            fare = 10 * distance;
            
            else  if(trav_class==2)
            fare = 15 * distance;
        }
        
        else
        fare = 7 * distance;
        
        System.out.println(fare);
    }
}
```






## OUTPUT:

<img width="332" height="265" alt="image" src="https://github.com/user-attachments/assets/579ee6db-831a-4ca9-aa8a-87cb54ffc259" />



## RESULT:

Thus, the Java program to calculate train ticket fare using conditional statements is implemented successfully
