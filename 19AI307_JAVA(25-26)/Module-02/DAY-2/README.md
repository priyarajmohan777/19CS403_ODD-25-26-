# Ex.No:2(B) METHODS

## QUESTION:
Create two methods:
Get the input for radius from the user.
double getArea(double r) → calculate the area and return the area(Don't print anything in this method).
void printArea(double area) → pass the calculated area to this method and print the area of a circle.

### For example:
<img width="136" height="90" alt="image" src="https://github.com/user-attachments/assets/80416685-7b01-4237-a621-833b30742bd2" />

## AIM:
To write a Java program to calculate and print the area of a circle using methods.

## ALGORITHM :
1.	Start the program.

2.	Import the package java.util and create a Scanner object to read input.

3.	Read the radius value from the user inside the main() method.

4.	Call the method getArea(double r) to calculate and return the area of the circle.

5.	Store the returned area value in a variable.

6.	Call the method printArea(double area) and pass the calculated area to print the result.

7.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
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
        double r = sc.nextDouble();
        double result = getArea(r);
        printArea(result);
    }
    
    static double getArea(double r)
    {
        double area = 3.14 * r * r;
        return area;
    }
    
    static void printArea(double area)
    {
        System.out.printf("%.2f" ,area);
    }
    
    
}
```

## OUTPUT:
<img width="334" height="149" alt="image" src="https://github.com/user-attachments/assets/5e7ac104-8fe0-4611-8b39-5d5f60d2aa99" />

## RESULT:
Thus, the Java program to calculate and print the area of a circle using methods is implemented successfully.
