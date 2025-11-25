# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)
For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

### For example:
<img width="342" height="223" alt="image" src="https://github.com/user-attachments/assets/236913ca-4a3b-41d9-a2e9-788fe1d0b588" />


## AIM:
To write a Java program using inheritance to calculate the final gold purchase price for different types of customers (general, regular, and premium) with discounts and cashback.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'.
3.	Create a base class Customer with attributes: customerId, name, purchaseWeight, goldRatePerGram.
4.	Define methods to calculate discount and final price.
5.	Create RegularCustomer class that extends Customer with 2% discount.
6.	Create PremiumCustomer class that extends Customer with 5% discount and 1% cashback.
7.	In the main method, read customer type, ID, name, weight, and gold rate.
8.	Create the appropriate customer object and call its display() method to show details.
9.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: PRIYA R
RegisterNumber: 212222040124 
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

    int getDiscountRate() {
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

    int getDiscountRate() {
        return 2;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    int getDiscountRate() {
        return 5;
    }

    double calculateCashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String customerType = sc.nextLine().trim();  
        String customerId = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double purchaseWeight = sc.nextDouble();
        double goldRatePerGram = sc.nextDouble();

        Customer c;

        if (customerType.equalsIgnoreCase("Regular")) {
            c = new RegularCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        } 
        else if (customerType.equalsIgnoreCase("Premium")) {
            c = new PremiumCustomer(customerId, name, purchaseWeight, goldRatePerGram);
        } 
        else {
            c = new Customer(customerId, name, purchaseWeight, goldRatePerGram);
        }

        c.display();
    }
}

```

## OUTPUT:

<img width="800" height="690" alt="image" src="https://github.com/user-attachments/assets/0feac762-7cba-40d0-817d-61d6ab7df257" />


## RESULT:
The program successfully calculates the final gold price for different customer types and displays discounts and cashback as applicable.

