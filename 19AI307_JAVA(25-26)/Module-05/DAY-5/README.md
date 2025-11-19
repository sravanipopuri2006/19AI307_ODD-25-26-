# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Synchronize deposit method in a BankAccount class, simulate deposits from multiple threads.


## AIM:
To simulate multiple concurrent deposits into a shared bank account using threads, ensuring thread-safety by synchronizing the deposit method.


## ALGORITHM :

<img width="1401" height="228" alt="image" src="https://github.com/user-attachments/assets/4a9407fd-1169-422b-b22a-2121798bfe24" />






## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Popuri sravani
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.*;

class BankAccount {
    private int balance = 0;

    public synchronized void deposit(int amount) {
        balance += amount;
    }

    public int getBalance() {
        return balance;
    }
}

class DepositTask extends Thread {
    BankAccount acc;
    int amount;

    DepositTask(BankAccount acc, int amount) {
        this.acc = acc;
        this.amount = amount;
    }

    public void run() {
        acc.deposit(amount);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        BankAccount acc = new BankAccount();
        DepositTask[] t = new DepositTask[n];

        for (int i = 0; i < n; i++) {
            int amount = sc.nextInt();
            t[i] = new DepositTask(acc, amount);
            t[i].start();
        }

        for (int i = 0; i < n; i++) {
            try { t[i].join(); } catch(Exception e) {}
        }

        System.out.println("Final Balance: " + acc.getBalance());
    }
}
```







## OUTPUT:

<img width="873" height="610" alt="image" src="https://github.com/user-attachments/assets/0a2594a3-cfea-49b5-ba20-38ac5b4102d0" />




## RESULT:
The program safely performs concurrent deposits using synchronized access and prints the correct final balance.

