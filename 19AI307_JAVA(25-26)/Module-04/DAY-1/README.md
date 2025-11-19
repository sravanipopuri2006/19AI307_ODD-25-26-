# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To write a Java program that demonstrates how a NullPointerException occurs when accessing methods on a null Integer object, and how to handle it using a try–catch block.


## ALGORITHM :
<img width="950" height="364" alt="image" src="https://github.com/user-attachments/assets/7f7ee2b0-5890-432b-b0d9-63e638b29d05" />





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Popuri sravani
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class NullPointerIntegerExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int input = sc.nextInt();
        Integer num = (input == 0) ? null : input;

        try {
            System.out.println(num.toString());
        } catch (NullPointerException e) {
            System.out.println("Null Integer");
        }

        sc.close();
    }
}
```







## OUTPUT:
<img width="834" height="383" alt="image" src="https://github.com/user-attachments/assets/5663b623-953b-4492-aaa0-4b1354be7bcd" />



## RESULT:

The program successfully demonstrates how invoking a method on a null Integer object triggers a NullPointerException, and shows how the exception can be caught and handled gracefully by printing "Null Integer"

