# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

### For example:
<img width="275" height="118" alt="image" src="https://github.com/user-attachments/assets/8029bc48-6a6b-43b5-83b8-ae56b262b0d3" />

## AIM:
To write a Java program that implements the Abstract Factory design pattern to create UI components (Button and Checkbox) for dark and light themes based on user choice.

## ALGORITHM :
1.	Start the program.
2.	Import java.util for user input.
3.	Create interfaces Button, Checkbox, and UIFactory.
4.	Create concrete classes for Dark and Light Button/Checkbox.
5.	Create factory classes DarkThemeFactory and LightThemeFactory implementing UIFactory.
6.	In main(), read theme selection and create the corresponding factory object.
7.	Use the factory to create and display button and checkbox objects.
8.	Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: PRIYA R
RegisterNumber: 212222040124 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Button {
    void render();
}

interface Checkbox {
    void render();
}

interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class DarkButton implements Button {
    public void render() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

class LightButton implements Button {
    public void render() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    public void render() {
        System.out.println("Light Checkbox created");
    }
}

class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }
    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        UIFactory factory;

        if (theme.equals("dark")) factory = new DarkThemeFactory();
        else if (theme.equals("light")) factory = new LightThemeFactory();
        else {
            System.out.println("Invalid theme");
            return;
        }

        factory.createButton().render();
        factory.createCheckbox().render();
    }
}
```

## OUTPUT:

<img width="602" height="281" alt="image" src="https://github.com/user-attachments/assets/93ddeb44-6e39-46ca-ae05-b19c80ba032f" />


## RESULT:

Thus, the Java program implementing the Abstract Factory design pattern to generate UI components for selected themes is executed successfully.
