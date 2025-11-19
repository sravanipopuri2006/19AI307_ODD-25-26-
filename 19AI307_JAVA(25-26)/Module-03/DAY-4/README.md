# Ex.No:3(D)    INTERFACE 

## QUESTION:
```
Two types of traffic controllers decide whether a vehicle can pass based on signal color. The decision logic varies by controller.

AggressiveController: Allows only if "GREEN".

DefensiveController: Allows for "GREEN" or "YELLOW".
```


## AIM:
To develop a Java program that decides whether a vehicle can move or must stop based on the signal color and the type of traffic controller (Aggressive or Defensive) using interfaces.


## ALGORITHM :
<img width="731" height="585" alt="image" src="https://github.com/user-attachments/assets/37036778-3bbf-4219-9ded-9e0e362f837f" />





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by:POPURI SRAVANI 
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;

interface TrafficController {
    boolean canGo(String signalColor);
}

class AggressiveController implements TrafficController {
    public boolean canGo(String signalColor) {
        return signalColor.equalsIgnoreCase("GREEN");
    }
}

class DefensiveController implements TrafficController {
    public boolean canGo(String signalColor) {
        return signalColor.equalsIgnoreCase("GREEN") || signalColor.equalsIgnoreCase("YELLOW");
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String color = sc.next();
        int type = sc.nextInt();

        TrafficController ctrl = (type == 1) ? new AggressiveController() : new DefensiveController();

        if (ctrl.canGo(color))
            System.out.println("GO");
        else
            System.out.println("STOP");
    }
}
```







## OUTPUT:
<img width="587" height="276" alt="image" src="https://github.com/user-attachments/assets/e3b3c827-e48c-419f-ae90-98fff1260fd5" />




## RESULT:
The program successfully determines whether a vehicle can move based on the signal color and controller type using interface-based polymorphism

