# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to reverse a number using a while loop. For example, if the input is 1234, the output should be 4321


## AIM:
To write a Java program that reverses a given number using a while loop.


## ALGORITHM :
=



## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by:  POPURI SRAVANI
RegisterNumber:  21223240117
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Sample
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int rev = 0;
        while (n!=0)
        {
            int digit = n%10;
            rev = (rev*10) + digit;
            n/=10;
        }
        System.out.print("Reversed number: "+rev);
    }
}
```







## OUTPUT:
<img width="556" height="236" alt="image" src="https://github.com/user-attachments/assets/196a209b-3391-452d-b21d-c80dbc223392" />




## RESULT:
The program successfully reverses the given number using a while loop and displays the reversed output.

