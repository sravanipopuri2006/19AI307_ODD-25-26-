# Ex.No:3(C) ABSTRACTION

## QUESTION:
```
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500
```

## AIM:
To write a Java program that uses an abstract class to calculate final game scores for two types of games:
ArcadeGame and PuzzleGame, each implementing its own scoring logic.


## ALGORITHM :
<img width="893" height="675" alt="image" src="https://github.com/user-attachments/assets/9bc28a3f-4882-4ff8-b8f1-be209cda80f3" />




## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: POPURI SRAVANI
RegisterNumber: 212223240117 
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class GameScore
{
    abstract int finalScore();
}

class ArcadeGame extends GameScore
{
    int base;
    int level;
    ArcadeGame(int base,int level)
    {
        this.base=base;
        this.level=level;
    }
    @Override
    int finalScore()
    {
        return (base+(level*100));
    }
}
class PuzzleGame extends GameScore
{
    int attempts;
    PuzzleGame(int attempts)
    {
        this.attempts=attempts;
    }
    @Override
    int finalScore()
    {
        return ((attempts <= 3) ? 1000 - (attempts * 100) : 500);
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        GameScore game;
        
        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }
        
        System.out.println(game.finalScore());
    }
}
```







## OUTPUT:
<img width="472" height="267" alt="image" src="https://github.com/user-attachments/assets/f12a95f0-b084-4030-ad7a-fb0973573cd8" />




## RESULT:
The program successfully calculates and displays the final score based on game type and user input using abstract methods and dynamic method dispatch.

