# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
```
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

Key Hint (Hidden in Story): Only one control tower object should exist.

Every flight contacting it should register its name.

You should log the order of flights that contacted the tower.
```

## AIM:
First line: Integer n – number of incoming flights

Next n lines: Each line contains the flight name.


## ALGORITHM :
<img width="983" height="706" alt="image" src="https://github.com/user-attachments/assets/719f15b0-a3e6-4342-812e-d94b4b602866" />





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Popuri sravani
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance;
    private int flightCount = 0;

    private RadarControlTower() {}

    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    public int registerFlight(String flightName) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();  // consume newline

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}
```







## OUTPUT:
<img width="1366" height="250" alt="image" src="https://github.com/user-attachments/assets/595d14a2-a364-40e4-9ad7-4c7040d27641" />




## RESULT:
The program successfully demonstrates the Singleton pattern by ensuring that all flights use the same Radar Control Tower instance. It registers each flight in order and displays the current total number of flights handled by the tower.

