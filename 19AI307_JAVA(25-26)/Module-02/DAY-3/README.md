# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program that creates a Person class with private attributes (name, age, country) and uses getter and setter methods to assign and retrieve values entered by the user.

## ALGORITHM :
<img width="735" height="520" alt="image" src="https://github.com/user-attachments/assets/6f1d24ad-4a22-4787-811c-0dcbf39c3ee5" />





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: POPURI SRAVANI 
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;
class Person {
     private String name;
     private int age;
     private String country;
     
     public String getName() {
          return name;
     }
     
     public void setName(String name) {
         this.name = name;
     }
     
     public int getAge() {
         return age;
     }
     
     public void setAge(int age) {
         this.age = age;
     }
     
     public void setCountry(String country) {
         this.country = country;
     }
     
     public String getCountry() {
         return country;
     }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        Person p = new Person();
        System.out.println("Person 1");
        p.setName(sc.next());
        System.out.println("Name: "+p.getName());
        p.setAge(sc.nextInt());
        System.out.println("Age: "+p.getAge());
        p.setCountry(sc.next());
        System.out.println("Country: "+p.getCountry());
    }
}
```







## OUTPUT:
<img width="863" height="516" alt="image" src="https://github.com/user-attachments/assets/5d985158-3fc2-4713-a9cc-08f6f5a227dc" />

## Result:
The program successfully accepts the name, age, and country of a person, stores them using setter methods, and displays the values using getter methods.







