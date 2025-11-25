# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to check if an element is present more than once in an array

### For example:
<img width="139" height="375" alt="image" src="https://github.com/user-attachments/assets/22a593ae-8a05-4841-a33e-79aa89741933" />

## AIM:
To write a Java program to check whether an element is repeated more than once in an array using nested loops.

## ALGORITHM :
1. Start the program.

2. Import the package java.util and create a Scanner object to read inputs.

3. Read the size of the array and store the elements into an integer array.

4. Initialize a boolean variable dupli as false.

5. Use a nested loop to compare each element with every other element in the array.

6. If any two elements are equal, set dupli = true and exit the loop.

7. If dupli is true, print "Yes", else print "No".

8. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        int size = sc.nextInt();
        int[] arr = new int[size];
        for(int i=0;i<size;i++)
        {
            arr[i] = sc.nextInt();
        }
        
        boolean dupli = false;
        for(int i=0;i<size;i++)
        {
            for(int j=i+1;j<size;j++)
            {
                if(arr[i]==arr[j])
                {
                    dupli = true;
                    break;
                }
            }
            if(dupli) break;
        }
        
        if(dupli)
        System.out.println("Yes");
        else
        System.out.println("No");
    }
}
```

## OUTPUT:

<img width="323" height="642" alt="image" src="https://github.com/user-attachments/assets/5ecedca9-7ed2-4474-928a-463e4ac08a57" />


## RESULT:
Thus, the Java program to check whether an element appears more than once in an array is implemented successfully
