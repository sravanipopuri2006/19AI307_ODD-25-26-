# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.


## AIM:
To write user information (name, age, email) into a text file using FileWriter and then read the same content using BufferedReader, demonstrating basic file handling in Java.

## ALGORITHM :

<img width="1288" height="361" alt="image" src="https://github.com/user-attachments/assets/e27959a6-e18e-4004-bb72-5ce00794fe03" />






## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Popuri sravani
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.io.*;
public class main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String fn = "userdata.txt";
        
        try
        {
            String name = sc.nextLine();
            int age = sc.nextInt();
            sc.nextLine();
            String mail = sc.nextLine();
            
            FileWriter fw = new FileWriter(fn);
            fw.write("User Information\n");
            fw.write("================\n");
            fw.write("Name  : "+name+"\n");
            fw.write("Age   : "+age+"\n");
            fw.write("Email : "+mail+"\n");
            fw.close();
            
            BufferedReader br = new BufferedReader(new FileReader(fn));
            String line;
            while((line = br.readLine())!=null)
            {
                System.out.println(line);
            }
            br.close();
        }
        catch(Exception e)
        {
            System.out.println("Error");
        }
    }
}
```







## OUTPUT:

<img width="998" height="346" alt="image" src="https://github.com/user-attachments/assets/2920730f-9556-447f-b075-5e6caaeb41ec" />




## RESULT:
The program successfully stores user details into a text file and reads them back line by line, displaying the stored content in the console.

