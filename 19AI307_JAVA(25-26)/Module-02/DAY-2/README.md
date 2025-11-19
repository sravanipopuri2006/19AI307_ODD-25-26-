# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).


## AIM:
To write a Java program that calculates the cube of a number using two separate methods:
one method to compute the square of a number
another method to compute the cube by using the square method.


## ALGORITHM :
<img width="412" height="219" alt="image" src="https://github.com/user-attachments/assets/127a0e6a-875d-46cf-b16f-671891c609d5" />

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by:Popuri Sravani 
RegisterNumber: 212223240117 
*/
```

## SOURCE CODE:
```
import java.util.*;

class A
{
    int cube(int x)
    {
       return x * square(x); 
    }
    
    int square(int x)
    {
        return x * x;
    }
}

public class Display
{
    public static void main(String[] args)
    {
        Scanner s = new Scanner(System.in);
        int x = s.nextInt();
        A a = new A();
        System.out.print(a.cube(x));
    }
}
```







## OUTPUT:
<img width="370" height="142" alt="image" src="https://github.com/user-attachments/assets/3bb02c5e-3c73-4aa8-945e-6c90ca7bf5a2" />




## RESULT:
The program successfully calculates the cube of the input number using method calling and displays the output.

