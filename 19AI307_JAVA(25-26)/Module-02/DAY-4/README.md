# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Implement a class Employee with a parameterized constructor to initialize id, name, and salary.


## AIM:
To write a Java program that creates an Employee object using a parameterized constructor and retrieves the employee details using getter methods.




## ALGORITHM :
<img width="949" height="573" alt="image" src="https://github.com/user-attachments/assets/697be318-8ec2-4bbf-a6ee-429ff28d1d17" />





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: POPURI SRAVANI
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;
class A
{
    int id;
    String name;
    float salary;
    A(int id, String name, float salary)
    {
        this.id = id;
        this.name = name;
        this.salary = salary;
    }
    
    public int get_id()
    {
        return id;
    }
    
    public String get_name()
    {
        return name;
    }
    
    public float get_salary()
    {
        return salary;
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner s = new Scanner(System.in);
        A a = new A(s.nextInt(), s.next(), s.nextFloat());
        System.out.println("Employee Details:");
        System.out.println("Employee ID: "+a.get_id());
        System.out.println("Employee Name: "+a.get_name());
        System.out.println("Employee Salary: "+a.get_salary());
    }
}
```







## OUTPUT:
<img width="1030" height="611" alt="image" src="https://github.com/user-attachments/assets/f55b3eb3-0a6f-4469-ba06-445803de8e45" />




## RESULT:
The program successfully creates an employee object using user input and displays the employee's ID, name, and salary using getter methods.

