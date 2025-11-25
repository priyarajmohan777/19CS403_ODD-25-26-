# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a base class Animal (Animal Family) with a method called Sound(). Create two subclasses Bird and Cat. Override the Sound() method in each subclass to make a specific sound for each animal.

### For example:
<img width="184" height="94" alt="image" src="https://github.com/user-attachments/assets/4034e0ec-28b0-4b3c-825c-921b16b9cea6" />

## AIM:
To write a Java program to demonstrate runtime polymorphism by overriding a method in subclasses to produce different sounds for different animals.

## ALGORITHM :
1.	Start the program.
2.	Import the package java.util to read user input.
3.	Create a base class Animal with a method Sound() that prints a default message.
4.	Create two subclasses Bird and Cat that extend Animal and override the Sound() method to print their specific sounds.
5.	In the main() method, read the animal type from the user.
6.	Based on user input, create an object of Bird, Cat, or Animal and assign it to the reference variable of type Animal.
7.	Call the Sound() method using the Animal reference to demonstrate runtime polymorphism.
8.	Stop the program.
   
## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: PRIYA R
RegisterNumber: 212222040124 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Animal {
    void Sound() {
        System.out.println("Animal makes a sound");
    }
}

class Bird extends Animal {
    @Override
    void Sound() {
        System.out.println("Bird chirps");
    }
}

class Cat extends Animal {
    @Override
    void Sound() {
        System.out.println("Cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String animalType = sc.nextLine().toLowerCase();

        Animal a;

        if (animalType.equals("bird")) {
            a = new Bird();
        } else if (animalType.equals("cat")) {
            a = new Cat();
        } else {
            a = new Animal();
        }

        a.Sound();
        sc.close();
    }
}
```

## OUTPUT:
<img width="567" height="243" alt="image" src="https://github.com/user-attachments/assets/04a5b0e2-36f0-4285-af4e-c174722e9202" />

## RESULT:
Thus, the Java program demonstrating polymorphism using method overriding in inheritance is implemented successfully.
