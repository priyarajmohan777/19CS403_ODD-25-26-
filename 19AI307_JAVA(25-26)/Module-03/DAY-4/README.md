# Ex.No:3(D)    INTERFACE 

## QUESTION:
You're building the equalizer system for a music app like BeatBoxx. The equalizer has 3 basic sound modes:

BassBoost
VocalBoost
Balanced
Each mode behaves differently and alters the sound experience. The app uses a SoundMode interface that each mode implements.

Input Format:
One line: Mode name (bass/vocal/balanced)

Output Format:
Display settings applied message for that mode

bass -  Print  "Bass Boost applied. Feel the beat drop!"
vocal - Print  "Vocal Boost enabled. Enjoy crystal-clear lyrics!"
balanced - Print  "Balanced mode set. A perfect blend of bass and vocals."
else - Print "Invalid mode selected."

### For example:

<img width="517" height="94" alt="image" src="https://github.com/user-attachments/assets/ae841e5c-1c55-4e97-ac47-8417b9fe5339" />


## AIM:
To write a Java program that demonstrates the use of interfaces by implementing different sound modes in a music equalizer system.

## ALGORITHM :
1.	Start the program.
2.	Import the package java.util to read user input.
3.	Create an interface SoundMode with an abstract method applyMode().
4.	Implement the interface in three classes: BassBoost, VocalBoost, and Balanced, each overriding applyMode() to print its specific message.
5.	In the main() method, read the mode name input from the user.
6.	Using a switch statement, based on the mode name, create the corresponding class object implementing SoundMode.
7.	If the mode entered is invalid, display "Invalid mode selected." and exit the program.
8.	Call the applyMode() method using the interface reference to display the selected mode’s output.
9.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: PRIYA R
RegisterNumber: 212222040124
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface SoundMode {
    void applyMode();
}


class BassBoost implements SoundMode {
    public void applyMode() {
        System.out.println("Bass Boost applied. Feel the beat drop!");
    }
}

class VocalBoost implements SoundMode {
    public void applyMode() {
        System.out.println("Vocal Boost enabled. Enjoy crystal-clear lyrics!");
    }
}

class Balanced implements SoundMode {
    public void applyMode() {
        System.out.println("Balanced mode set. A perfect blend of bass and vocals.");
    }
}


public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String mode = sc.nextLine().toLowerCase();

        SoundMode soundMode;

        switch (mode) {
            case "bass":
                soundMode = new BassBoost();
                break;
            case "vocal":
                soundMode = new VocalBoost();
                break;
            case "balanced":
                soundMode = new Balanced();
                break;
            default:
                System.out.println("Invalid mode selected.");
                return;
        }

        soundMode.applyMode();
    }
}
```

## OUTPUT:
<img width="1184" height="261" alt="image" src="https://github.com/user-attachments/assets/e8295e65-b1b6-496e-aede-c3f1941c662f" />

## RESULT:
Thus, the Java program implementing an interface to switch between different sound modes in an equalizer is executed successfully.
