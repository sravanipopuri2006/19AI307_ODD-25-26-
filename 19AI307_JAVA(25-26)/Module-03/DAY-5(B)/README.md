# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to find the square root of a number using Double wrapper class.


## AIM:
To write a Java program that reads a number in string format, converts it into a double, and prints its square root using the Math.sqrt() function.


## ALGORITHM :
<img width="655" height="266" alt="image" src="https://github.com/user-attachments/assets/2501673b-0081-4fb6-b756-a73b65544e98" />






## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: POPURI SRAVANI
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;

public class Main
{
    public static void main(String[] args)
    {
        Scanner s = new Scanner(System.in);
        String str = s.next();
        
        Double num = Double.parseDouble(str);
        System.out.println("Square root of "+num+" is: "+(Math.sqrt(num)));
    }
}
```







## OUTPUT:
<img width="1191" height="376" alt="image" src="https://github.com/user-attachments/assets/151b13e6-9cab-408c-928f-473d0b978aac" />




## RESULT:
The program successfully reads a numeric string, converts it to a double value, computes its square root, and displays the result.

