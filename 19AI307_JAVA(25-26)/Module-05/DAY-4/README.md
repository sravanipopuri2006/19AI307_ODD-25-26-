# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.
Note : Read the threadname from the User


## AIM:
To create and execute a thread using the Runnable interface, set its name from user input, and display thread properties such as priority and name.


## ALGORITHM :

<img width="1109" height="212" alt="image" src="https://github.com/user-attachments/assets/426bfe18-2cf7-49c5-a85e-6cdcc29b0e0f" />





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Popuri sravani
RegisterNumber:212223240117  
*/
```

## SOURCE CODE:
```
import java.util.*;

public class A implements Runnable {
    public void run() {
        System.out.println(Thread.currentThread());
    }

    public static void main(String[] args) {
        A a = new A();
        Scanner sc = new Scanner(System.in);
        String thname = sc.nextLine();
        Thread t = new Thread(a, thname);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        t.start();
    }
}
```







## OUTPUT:

<img width="991" height="266" alt="image" src="https://github.com/user-attachments/assets/6c14265e-c0b3-4845-b17d-c270b8a13f37" />




## RESULT:
The program successfully creates a thread with a user-given name, prints its priority and name, and displays the thread details when executed.

