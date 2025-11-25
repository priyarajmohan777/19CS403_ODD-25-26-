# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a java program to check whether a string is a palindrome.

### For example:

<img width="283" height="111" alt="image" src="https://github.com/user-attachments/assets/c127c5c6-dc25-4851-be18-c4634e15ac7a" />


## AIM:
To write a Java program to check whether a given string is a palindrome using string functions and looping.

## ALGORITHM :

1.Start the program.

2. Import the package java.util and create a Scanner object to read input from the user.

3. Read the string input and store it in a variable.

4. Initialize a boolean variable isPalindrome to true.

5. Use a for loop to compare characters from the beginning and end of the string.

6. If any character pair does not match, set isPalindrome = false and break the loop.

7. If isPalindrome is true, print that the string is a palindrome; otherwise print that it is not.

8. Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: PRIYA R
RegisterNumber: 212222040124
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
        String word = sc.next();
        boolean isPalindrome =true;
        
        for(int start=0,end=word.length()-1;start<end;start++,end--)
        {
            if(word.charAt(start)!=word.charAt(end))
            {
                isPalindrome = false;
                break;
            }
            
        }
        
        if(isPalindrome)
        {
            System.out.print(word + " is a palindrome.");
        }
        else
        {
            System.out.print(word + " is not a palindrome.");
        }
    }
}
```


## OUTPUT:

<img width="729" height="236" alt="image" src="https://github.com/user-attachments/assets/6d33457c-ba24-4a34-a0f7-60392cb2e8d2" />


## RESULT:
Thus, the Java program to check whether a string is a palindrome using strings and looping statements is implemented successfully.
