# Ex.No:3(C) ABSTRACTION

## QUESTION:
In a secret facility, you are designing intelligent agents that can explore grid-based mazes. Each agent sees the maze differently and interprets it using their unique instinct.

You are to build a system using abstraction where a base class MazeAgent declares an abstract method:
abstract String generateNavigationCode(String[] maze);
Two agents – ScoutAgent and HunterAgent – extend this class, but behave very differently.

Agent Behaviors
ScoutAgent
This agent is highly sensitive to special signals placed in the maze. Every time it senses the signal (@), it records where (which corridor row) the signal was found.
The final navigation code is the sequence of all those rows where it felt the signal — encoded as numbers.

HunterAgent
This agent is on the lookout for how trapped it might be. It keeps a strict count of all obstructions it sees in the maze walls.
If the number of such obstructions is equal or more than 10, it believes it's been trapped. Otherwise, it considers itself safe to escape.

Your Task:
Implement the abstract class and its derived classes.
Accept maze rows as input.
Create the agent based on input.
Print the navigation code they generate.

### For example:
<img width="148" height="355" alt="image" src="https://github.com/user-attachments/assets/54908f4c-a5ea-449d-bf4b-7caefe212492" />


## AIM:
To write a Java program that demonstrates abstraction by defining an abstract class with an abstract method and implementing different navigation behaviors in derived agent classes.

## ALGORITHM :
1.	Start the program.
2.	Import the package java.util for user input.
3.	Create an abstract class MazeAgent containing an abstract method generateNavigationCode(String[] maze).
4.	Create the derived class ScoutAgent that overrides the abstract method to detect signal occurrences (@) in maze rows and generate a navigation code based on signal locations.
5.	Create another derived class HunterAgent that overrides the method to count wall obstructions (#) and return "TRAPPED" if count ≥ 10, otherwise "ESCAPE".
6.	In the main() method, read the number of maze rows and read each row into a string array.
7.	Read the agent type from the user and dynamically create either ScoutAgent or HunterAgent using abstraction.
8.	Call the generateNavigationCode() method using the base class reference and print the result.
9.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: PRIYA R
RegisterNumber: 212222040124
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class MazeAgent {
    abstract String generateNavigationCode(String[] maze);
}

class ScoutAgent extends MazeAgent {
    @Override
    String generateNavigationCode(String[] maze) {
        StringBuilder code = new StringBuilder();

        for (int i = 0; i < maze.length; i++) {
            String row = maze[i];
            int signals = 0;
            for (int j = 0; j < row.length(); j++) {
                if (row.charAt(j) == '@') {
                    signals++;
                }
            }
            for (int k = 0; k < signals; k++) {
                code.append(i + 1);
            }
        }

        return code.toString();
    }
}

class HunterAgent extends MazeAgent {
    @Override
    String generateNavigationCode(String[] maze) {
        int count = 0;

        for (String row : maze) {
            for (char c : row.toCharArray()) {
                if (c == '#') {
                    count++;
                }
            }
        }

        if (count >= 10) {
            return "TRAPPED";
        } else {
            return "ESCAPE";
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        sc.nextLine();

        String[] maze = new String[n];
        for (int i = 0; i < n; i++) {
            maze[i] = sc.nextLine();
        }

        int type = sc.nextInt();

        MazeAgent agent;

        if (type == 1) {
            agent = new ScoutAgent();
        } else {
            agent = new HunterAgent();
        }

        System.out.println(agent.generateNavigationCode(maze));

        sc.close();
    }
}
```

## OUTPUT:

<img width="350" height="548" alt="image" src="https://github.com/user-attachments/assets/d14ad674-de63-47b3-b0d6-867939564567" />

## RESULT:

Thus, the Java program demonstrating abstraction using abstract classes and overridden methods for customized agent behavior is implemented successfully.
