# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the index of a given element in an array.


## AIM:
To write a Java program that performs a linear search on an array to find the index/indices of a target element entered by the user.


## ALGORITHM :
```
1.Start the program.
2.Read an integer n representing the size of the array.
3.Create an integer array of size n.
4.Read n elements from the user and store them in the array.
5.Read the target element to be searched.
6.Initialize a boolean variable flag = false.
7.Traverse the array from index 0 to n - 1:
8.If arr[i] == target:
    Set flag = true
    Print the index i
  After completing the loop:
  If flag is still false, print "Element not found".
9.End the program.
```




## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: POPURI SRAVANI
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Demo
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i<n; i++) arr[i] = sc.nextInt();
        int target=sc.nextInt();
        boolean flag = false;
        for (int i = 0; i<n; i++)
        {
            if (arr[i] == target)
            {
                flag = true;
                System.out.println(i);
            }
        }
        if (flag == false) System.out.println("Element not found");
    }
}
```
## OUTPUT:
<img width="548" height="425" alt="image" src="https://github.com/user-attachments/assets/34b2b7c8-c722-43d4-89fa-aafed298fe5f" />
## Result:
The program successfully performs a linear search on the user-entered array and displays the index/indices where the target element is found. If the target does not exist in the array, it prints "Element not found".




## RESULT:

