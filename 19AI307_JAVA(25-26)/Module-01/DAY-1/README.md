# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely found a magic machine that tells her how two numbers relate to each other. The machine supports all 6 relational operators:
<img width="296" height="234" alt="image" src="https://github.com/user-attachments/assets/3c9159bf-95ec-4332-b2c3-454378ae1930" />
<br/>
Lovely enters two numbers. The machine prints the result (true or false) for each operator.
## Input Format
```
First line: First integer number (a)

Second line: Second integer number (b)
## Output format
a == b: <true/false>
a != b: <true/false>
a > b: <true/false>
a < b: <true/false>
a >= b: <true/false>
a <= b: <true/false>
```
## AIM:
To read two integer values from the user and display the results of all six relational operations (==, !=, >, <, >=, <=) between them.


## ALGORITHM :
```
1.Start the program.
2.Import the Scanner class to read user input.
3.Create a Scanner object.
4.Read the first integer a.
5.Read the second integer b.
6.Evaluate and print the result of:
a == b
a != b
a > b
a < b
a >= b
a <= b
7.End the program.
```



## PROGRAM:
 ```

Program to implement variables and Operators using Java
Developed by: POPURI SRAVANI
RegisterNumber:  212223240117

```

## Sourcecode.java:
```
import java.util.*;
public class Sample
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        System.out.println("a == b: "+(a==b));
        System.out.println("a != b: "+(a!=b));
        System.out.println("a > b: "+(a>b));
        System.out.println("a < b: "+(a<b));
        System.out.println("a >= b: "+(a>=b));
        System.out.println("a <= b: "+(a<=b));
    }
}
```
## OUTPUT:
<img width="501" height="245" alt="image" src="https://github.com/user-attachments/assets/7ae02937-3e39-47f7-9a8e-2a71d967f8b6" />

## Result:
The program successfully reads two integers and displays the results of all relational operators (==, !=, >, <, >=, <=) correctly based on the given inputs.




