# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class City with attributes: cityName (String), population (long), area (double). Create an object. Print all details.

### For example:
<img width="281" height="229" alt="image" src="https://github.com/user-attachments/assets/55425019-e2f3-4559-a6cf-cd9e1f1e0a5f" />

## AIM:
To write a Java program to create a class City with attributes and an object to display the city details using class and object concepts.

## ALGORITHM :

1. Start the program.

2. Import the package java.util to accept user inputs.

3. Create a class City with data members: cityName, population, and area.

4. Define a method printDetails() to display the values of these attributes.

5. In the main() method, create an object of the City class.

6. Read the values for cityName, population, and area from the user and assign them to object variables.

7. Call the printDetails() method to display the city information.

8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: PRIYA R
RegisterNumber:  212222040124
*/
```

## SOURCE CODE:

```
import java.util.*;
class City
{
    String cityName;
    long population;
    double area;
    
    void printDetails()
    {
        System.out.println("City Name: " + cityName);
        System.out.println("Population: " + population);
        System.out.println("Area: " + area);
    }
}
class prog
{
  public static void main(String[] args)
  {
    Scanner sc = new Scanner(System.in);
 
    City obj = new City();
    obj.cityName = sc.nextLine();
    obj.population = sc.nextLong();
    obj.area = sc.nextDouble();
    obj.printDetails();
  }
}
```

## OUTPUT:

<img width="575" height="372" alt="image" src="https://github.com/user-attachments/assets/4ff4408b-a215-4cb4-8649-d5d040cc618b" />


## RESULT:
Thus, the Java program using class and object concepts to display city details is implemented successfully.

