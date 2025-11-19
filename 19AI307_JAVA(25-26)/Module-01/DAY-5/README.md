# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to count the frequency of a given character in a string.



## AIM:


## ALGORITHM :
<img width="401" height="233" alt="image" src="https://github.com/user-attachments/assets/a643d28c-30aa-4969-b7a9-0cf5e51e0141" />






## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: POPURI SRAVANI
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;
public class A
{
    public static void main(String[] args)
    {
        Scanner s = new Scanner(System.in);
        String str = s.next();
        Character c = s.next().charAt(0);
        int count = 0;
        for (int i = 0; i < str.length(); i++)
        {
            if (str.charAt(i) == c) count++;
        }
        System.out.print("Frequency of '"+c+"' is: "+count);
    }
}
```







## OUTPUT:
<img width="564" height="255" alt="image" src="https://github.com/user-attachments/assets/7e850a3e-f018-4e3b-a4f9-e4072e0d2537" />




## RESULT:
The program successfully counts and displays the number of times a given character occurs in the input string.

