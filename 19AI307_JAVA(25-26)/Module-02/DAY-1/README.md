# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

## AIM:
To write a Java program that creates a Vehicle class with attributes number, type, and owner, then reads the details of two vehicle objects and displays them.




## ALGORITHM :
<img width="571" height="431" alt="image" src="https://github.com/user-attachments/assets/a2e6afe2-3481-4dd0-a23b-2af48a5f6d98" />
	





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: POPURI SRAVANI
RegisterNumber:212223240117  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Vehicle
{
    String number;
    String type;
    String owner;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}
```







## OUTPUT:
<img width="952" height="282" alt="image" src="https://github.com/user-attachments/assets/a219cfa6-7f01-40f9-bf35-933cce54754e" />




## RESULT:
The program successfully creates two Vehicle objects, reads their details from the user, and prints them in the specified format.

