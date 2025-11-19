# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).


## AIM:
To develop a Java program that calculates the final gold purchase amount for different customer types using inheritance.
The program should apply:
2% discount for RegularCustomer
5% discount + 1% cashback for PremiumCustomer
and compute the final payable amount based on purchase weight and gold rate per gram.


## ALGORITHM :
<img width="808" height="793" alt="image" src="https://github.com/user-attachments/assets/43fb2e5c-a13b-4b50-927f-f54796a55cb8" />





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: POPURI SRAVANI
RegisterNumber:  212223240117
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 2.0;
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() {
        return 5.0;
    }

    double getCashback() {
        return calculateFinalPrice() * 0.01;
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

public class JewelryStore {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.nextLine().trim();
        String customerId = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double purchaseWeight = sc.nextDouble();
        double goldRatePerGram = sc.nextDouble();

        Customer customer;
        if (type.equalsIgnoreCase("Regular")) {
            customer = new RegularCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        } else if (type.equalsIgnoreCase("Premium")) {
            customer = new PremiumCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        } else {
            customer = new Customer(customerId, name, purchaseWeight, goldRatePerGram);
        }

        customer.display();
    }
}
```







## OUTPUT:
<img width="967" height="698" alt="image" src="https://github.com/user-attachments/assets/a9c4bcd1-c05b-4294-ac0d-26f1d1588b80" />




## RESULT:
The program successfully computes the final gold purchase price for:
General customers
Regular customers (with 2% discount)
Premium customers (with 5% discount and 1% cashback)
It displays complete details including customer type, discount applied, final price, and cashback for premium customers.

