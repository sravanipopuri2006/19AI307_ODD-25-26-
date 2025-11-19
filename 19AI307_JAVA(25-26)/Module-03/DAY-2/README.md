# Ex.No:3(b) POLYMORPHISM

## QUESTION:
```
Write a Java program using method overloading to print student details. Create a class Student with:
print(String name)
print(String name, int age)
print(String name, int age, String dept)
```


## AIM:
To write a Java program that demonstrates method overloading by printing student details using three versions of the print() method with different parameter lists


## ALGORITHM :
<img width="961" height="387" alt="image" src="https://github.com/user-attachments/assets/5e22bf89-856e-4daa-b6b5-ee77dd91ac08" />






## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: POPURI SRAVANI
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Student {
    public static void print(String name) {
        System.out.println("Name: " + name);
    }

    public static void print(String name, int age) {
        System.out.println("Name: " + name + ", Age: " + age);
    }

    public static void print(String name, int age, String dept) {
        System.out.println("Name: " + name + ", Age: " + age + ", Dept: " + dept);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String name1 = scanner.nextLine();
        print(name1);

        String name2 = scanner.nextLine();
        int age2 = scanner.nextInt();
        scanner.nextLine(); 
        print(name2, age2);

        String name3 = scanner.nextLine();
        int age3 = scanner.nextInt();
        scanner.nextLine();
        String dept3 = scanner.nextLine();
        print(name3, age3, dept3);
    }
}
```







## OUTPUT:
<img width="933" height="632" alt="image" src="https://github.com/user-attachments/assets/530efe6b-71e3-4a1d-b11d-72b4a55432ef" />




## RESULT:
The program successfully demonstrates method overloading by printing student details using three different method signatures based on the number of arguments passed.

