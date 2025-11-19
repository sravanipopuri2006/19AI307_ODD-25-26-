# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)


## AIM:
To demonstrate stream chaining in Java by combining InputStreamReader and BufferedReader to read user input efficiently from System.in.To demonstrate stream chaining in Java by combining InputStreamReader and BufferedReader to read user input efficiently from System.in.


## ALGORITHM :

<img width="984" height="227" alt="image" src="https://github.com/user-attachments/assets/1a6f670b-b770-451b-a9f8-6dc96e489c43" />






## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Popuri sravani
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        // Chaining: System.in -> InputStreamReader -> BufferedReader
        try (BufferedReader br = new BufferedReader(new InputStreamReader(System.in))) {
            
            String name = br.readLine();   // reading input using BufferedReader

            String ageStr = br.readLine(); // reading another line
            int age = Integer.parseInt(ageStr);

            System.out.println("--- User Details ---");
            System.out.println("Name: " + name);
            System.out.println("Age: " + age);

        } catch (IOException e) {
            System.out.println("An error occurred while reading input: " + e.getMessage());
        }
    }
}
```







## OUTPUT:

<img width="800" height="574" alt="image" src="https://github.com/user-attachments/assets/f1c8ee61-e293-43e8-8323-1ae386550b21" />




## RESULT:
The program successfully reads multiple lines of user input using chained input streams and prints the user details. It demonstrates effective use of BufferedReader wrapped around InputStreamReader for fast and efficient input handling.

