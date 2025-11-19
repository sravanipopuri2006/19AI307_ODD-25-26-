# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".


## AIM:
To write a Java program that demonstrates the use of:
an instance method to perform addition,
a static method to display information, and calculates the sum of two numbers entered by the user.


## ALGORITHM :
<img width="1082" height="407" alt="image" src="https://github.com/user-attachments/assets/9a684126-cf0b-4f3c-b980-fa011e472b04" />





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: POPURI SRAVANI
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Calculator {
    // Your Methods here
    int add(int a, int b)
    {
        return a+b;
    }
    
    static void info()
    {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        // Your Function Initiation here
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        Calculator c = new Calculator();
        Calculator.info();
        System.out.println("Sum: "+c.add(a,b));
    }
}
```







## OUTPUT:
<img width="993" height="413" alt="image" src="https://github.com/user-attachments/assets/8b7619fe-7956-4ab6-a310-0cb7dcd04677" />




## RESULT:
The program successfully demonstrates the use of instance and static methods by displaying a message through the static method and printing the sum of two numbers using the instance method.

