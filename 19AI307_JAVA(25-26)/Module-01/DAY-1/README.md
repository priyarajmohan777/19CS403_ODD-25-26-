# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is entering a battle arena tournament, but only heroes who meet specific power and skill criteria are allowed inside.
To enter the arena, a hero (Lovely) must satisfy any one of these conditions:
Her power level is above 80 and her rank is above 5
→ (power > 80 && rank > 5)

Or she has a magic orb and her experience is at least 3 years
→ (hasMagicOrb == true && experience >= 3)

Note: If either of the above conditions is satisfied, she is allowed to enter. Otherwise, she is rejected.

### For example:

<img width="282" height="277" alt="image" src="https://github.com/user-attachments/assets/ee39b974-a08b-4151-b75b-fdab6b0709fb" />


## AIM:

To write a Java program to implement variables and logical operators to check whether a hero can enter the battle arena based on given conditions.

## ALGORITHM :
1.	Start the program

2. Accept input from the user for power, rank, magic orb availability, and experience.

3. Store the values in appropriate variables.

4. Check if power is greater than 80 and rank is greater than 5.

5. Otherwise, check if the hero has a magic orb and experience is at least 3 years.

6. If either condition is satisfied, display "Can Enter Arena: true", else display "Can Enter Arena: false".

7. Stop the program.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: PRIYA R
RegisterNumber:  212222040124
*/
```

## Sourcecode.java:

```
import java.util.*;
public class Arena
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int power = sc.nextInt();
        int rank = sc.nextInt();
        boolean hasMagicOrb = sc.nextBoolean();
        int exp = sc.nextInt();
        
        if((power>80 && rank>5) || (hasMagicOrb && exp>=3))
        System.out.print("Can Enter Arena: true");
        
        else
        System.out.print("Can Enter Arena: false");
    }
}

```


## OUTPUT:

<img width="607" height="560" alt="image" src="https://github.com/user-attachments/assets/3851df3c-fd50-4075-8378-0474d5c01cc2" />



## RESULT:

Thus, the Java program to check arena entry eligibility using variables and logical operators is executed successfully


