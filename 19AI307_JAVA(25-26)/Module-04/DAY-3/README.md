# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:

Simulate a fan speed controller using the State Pattern. Each time the user types "next", change fan speed from Off -> Low -> Medium -> High -> Off.

## AIM:

To Simulate a fan speed controller using the State Pattern. Each time the user types "next", change fan speed from Off -> Low -> Medium -> High -> Off.
## ALGORITHM :
1.Start program.

2.Create a State interface with a method next(Fan fan) and getName().

3.Implement four concrete states: OffState, LowState, MediumState, HighState. Each state's next method sets the fan's state to the appropriate next state.

4.Create Fan class that holds a reference to current State and has a pressNext() method that delegates to the state's next() and prints the current state.

5.In main(), read user input lines. For each line: if it is "next" call fan.pressNext(); if it is "exit" terminate.

6.End the program.



## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Jeevansurya k
RegisterNumber: 212222040061
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface FanState {
    void next(Fan fan);
    void printState();
}
class OffState implements FanState {
    public void next(Fan fan) {
        fan.setState(new LowState());
    }
    public void printState() {
        System.out.println("Fan is Off");
    }
}

class LowState implements FanState {
    public void next(Fan fan) {
        fan.setState(new MediumState());
    }
    public void printState() {
        System.out.println("Fan is on Low");
    }
}

class MediumState implements FanState {
    public void next(Fan fan) {
        fan.setState(new HighState());
    }
    public void printState() {
        System.out.println("Fan is on Medium");
    }
}

class HighState implements FanState {
    public void next(Fan fan) {
        fan.setState(new OffState());
    }
    public void printState() {
        System.out.println("Fan is on High");
    }
}
class Fan {
    private FanState state;

    public Fan() {
        state = new OffState();
    }

    public void setState(FanState state) {
        this.state = state;
        state.printState();
    }

    public void pressButton() {
        state.next(this);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Fan fan = new Fan();
        while (true) {
            String input = scanner.nextLine();
            if (input.equalsIgnoreCase("exit")) break;
            if (input.equalsIgnoreCase("next")) fan.pressButton();
        }
    }
}
```





## OUTPUT:

<img width="676" height="514" alt="image" src="https://github.com/user-attachments/assets/25d1b51d-b4e4-44af-b69f-d22ff3ae5c37" />



## RESULT:
Thus, the program executed successfully.
