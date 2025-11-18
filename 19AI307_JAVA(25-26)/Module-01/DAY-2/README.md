# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
```
You are given the lengths of three sides of a triangle. Determine whether the triangle is:

Equilateral – all sides equal
Isosceles – two sides equal
Scalene – all sides different
If the sides don’t form a valid triangle (triangle inequality fails), print:

Not a triangle
```


## AIM:
To read three side lengths of a triangle and determine whether the triangle is Equilateral, Isosceles, Scalene, or Not a triangle based on the triangle inequality rules.


## ALGORITHM :
```
1.Start the program.
2.Create an integer array of size 3.
3.Read three integers from the user and store them in the array.
4.Assign the values to variables a, b, and c.
5.Check the triangle inequality condition:
6.If (a + b <= c) OR (a + c <= b) OR (b + c <= a):
7.Print "Not a triangle".
8.If the above condition is false:
9.If all three sides are equal (a == b and a == c):
10.Print "Equilateral".
11.Else if any two sides are equal (a == b or a == c or b == c):
Print "Isosceles".
Else:
Print "Scalene".
12.End the program.
```



## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
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
        int arr[] = new int[3];
        for (int i=0; i<3; i++) arr[i] = s.nextInt();
        
        int a = arr[0], b = arr[1], c = arr[2];
        
        if (a+b<=c || a+c<=b || b+c<=a) System.out.print("Not a triangle");
        else if (a==b && a==c) System.out.print("Equilateral");
        else if (a == b || a == c || b == c) System.out.print("Isosceles");
        else
        {
            System.out.print("Scalene");
        }
    }
}
```







## OUTPUT:
<img width="533" height="132" alt="image" src="https://github.com/user-attachments/assets/fcc64fcc-a71f-4389-81ed-e6c08682c3a3" />
## RESULT:
The program successfully reads three side lengths, applies triangle inequality rules, and correctly identifies the triangle as Equilateral, Isosceles, Scalene, or Not a triangle.

