# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).


## AIM:
To write a Java program that demonstrates composition, where a Library contains multiple Book objects.
The program should accept book details from the user, store them inside a Library object, and display all stored books.


## ALGORITHM :
<img width="750" height="655" alt="image" src="https://github.com/user-attachments/assets/cdb3c9b3-6820-4497-a128-dc2fa3cb8bfc" />





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Popuri sravani
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }
        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    String getDetails() {
        return "- " + title + " by " + author;
    }
}

class Library {
    private List<Book> books;

    Library() {
        books = new ArrayList<>();
    }

    void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books)
            System.out.println(b.getDetails());
    }
}
```







## OUTPUT:
<img width="926" height="508" alt="image" src="https://github.com/user-attachments/assets/ec42dba2-aa6c-4284-b236-e6546676bb98" />




## RESULT:
The program successfully demonstrates composition by creating a Library object that holds multiple Book objects. It reads book details from the user, stores them inside the library, and displays all the books in a structured format.

