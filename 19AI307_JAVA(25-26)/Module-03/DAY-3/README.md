# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().

## AIM:
To Create abstract class GameScore with method finalScore().

## ALGORITHM :
1.Start the program.

2.Create an abstract class GameScore containing an abstract method finalScore().

3.Create a subclass CricketScore that extends GameScore and implements finalScore() to display the cricket score.

4.Create another subclass FootballScore that extends GameScore and implements finalScore() to display the football score.

5.In main(), create objects of both subclasses and call their finalScore() methods.

6.End the program.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Jeevansurya k
RegisterNumber: 212222040061
*/
```

## SOURCE CODE:

```
import java.util.*;

// Abstract class
abstract class GameScore {
    abstract int finalScore();
}

// ArcadeGame subclass
class ArcadeGame extends GameScore {
    int baseScore, level;

    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    @Override
    int finalScore() {
        return baseScore + (level * 100);
    }
}

// PuzzleGame subclass
class PuzzleGame extends GameScore {
    int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    @Override
    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();

        GameScore game;

        if (type == 1) { // ArcadeGame
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else { // PuzzleGame
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }

        System.out.println(game.finalScore());
    }
}
```


## OUTPUT:

<img width="446" height="338" alt="image" src="https://github.com/user-attachments/assets/d7a5b9da-d287-4a0b-a278-e9335dd38270" />

## RESULT:
Thus the program executed successfully.

## RESULT:

