# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an MVC program for a School System where the DAO stores student info, controller fetches it, and view displays it.


## AIM:
To implement a simple Student Management System using the MVC (Model–View–Controller) architecture along with the DAO (Data Access Object) pattern, enabling student data storage, retrieval, and display based on roll number.


## ALGORITHM :

<img width="558" height="849" alt="image" src="https://github.com/user-attachments/assets/f95157fb-006b-4ce4-acc8-462925462c6a" />
	





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: popuri sravani
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;

// Model
class Student {
    private String name;
    private int age;
    private String rollNo;

    public Student(String name, int age, String rollNo) {
        this.name = name;
        this.age = age;
        this.rollNo = rollNo;
    }

    public String getName() { return name; }
    public int getAge() { return age; }
    public String getRollNo() { return rollNo; }
}

// DAO Interface
interface StudentDAO {
    void addStudent(Student student);
    Student getStudentByRollNo(String rollNo);
}

// DAO Implementation
class StudentDAOImpl implements StudentDAO {
    private List<Student> students = new ArrayList<>();

    public void addStudent(Student student) {
        students.add(student);
    }

    public Student getStudentByRollNo(String rollNo) {
        for (Student s : students) {
            if (s.getRollNo().equalsIgnoreCase(rollNo)) {
                return s;
            }
        }
        return null;
    }
}

// View
class StudentView {
    public void displayStudent(Student student) {
        if (student != null) {
            System.out.println("Student Details:");
            System.out.println("Name    : " + student.getName());
            System.out.println("Age     : " + student.getAge());
            System.out.println("Roll No : " + student.getRollNo());
        } else {
            System.out.println("Student not found.");
        }
    }
}

// Controller
class StudentController {
    private StudentDAO dao;
    private StudentView view;

    public StudentController(StudentDAO dao, StudentView view) {
        this.dao = dao;
        this.view = view;
    }

    public void addStudent(Student student) {
        dao.addStudent(student);
    }

    public void showStudent(String rollNo) {
        Student student = dao.getStudentByRollNo(rollNo);
        view.displayStudent(student);
    }
}

// Main (Test Case)
public class SchoolSystemMVC {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        StudentDAO dao = new StudentDAOImpl();
        StudentView view = new StudentView();
        StudentController controller = new StudentController(dao, view);

        int n = sc.nextInt();
        sc.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            int age = Integer.parseInt(sc.nextLine());
            String roll = sc.nextLine();
            controller.addStudent(new Student(name, age, roll));
        }

        String searchRollNo = sc.nextLine();
        controller.showStudent(searchRollNo);

        sc.close();
    }
}
```







## OUTPUT:

<img width="938" height="777" alt="image" src="https://github.com/user-attachments/assets/57ae061b-0207-4f2c-888d-6d753eed8a6c" />




## RESULT:
The program successfully demonstrates the MVC + DAO architecture for managing student data. It stores multiple student records, retrieves a student based on roll number, and displays the result through the view component.

