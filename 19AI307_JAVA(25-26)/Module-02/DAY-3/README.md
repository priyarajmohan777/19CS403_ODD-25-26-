# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

### For example:
<img width="295" height="151" alt="image" src="https://github.com/user-attachments/assets/4044f435-f734-4f39-aa65-625632bccbd2" />


## AIM:
To write a Java program to demonstrate the use of access specifiers by declaring private variables in a class and accessing them using public getter and setter methods.

## ALGORITHM :
1.	Start the program.

2.	Import the package java.util to read input from the user.

3.	Create a class Person with private data members: name, age, and country.

4.	Define public getter and setter methods for each private variable to access and modify their values.

5.	In the main() method, create an object of the Person class.

6.	Read input values from the user and assign them through setter methods.

7.	Display the values using getter methods.

8.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: PRIYA R
RegisterNumber: 212222040124 
*/
```

## SOURCE CODE:

```
import java.util.*;
public class Person {
  
    private String name;
    private int age;
    private String country;

    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    
    public int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }
    
    public String getCountry() {
        return country;
    }
    public void setCountry(String country) {
        this.country = country;
    }
        
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String name = sc.next();
        int age = sc.nextInt();
        String country = sc.next();
        
        Person p1 = new Person();
        p1.setName(name);
        p1.setAge(age);
        p1.setCountry(country);
        
        System.out.println("Person 1");
        System.out.println("Name: " + p1.getName());
        System.out.println("Age: " + p1.getAge());
        System.out.println("Country: " + p1.getCountry());
        
    
    }
}

```

## OUTPUT:
<img width="715" height="454" alt="image" src="https://github.com/user-attachments/assets/e06e59bc-f277-469b-af7c-2f33cf8d795f" />

## RESULT:
Thus, the Java program demonstrating the use of access specifiers with getter and setter methods is implemented successfully.
