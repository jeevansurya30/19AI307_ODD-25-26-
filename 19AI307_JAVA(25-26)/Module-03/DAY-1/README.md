# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A fuel station sells two types of fuels: Petrol and Diesel.

There is a base class named Fuel, which has the following attributes: fuelId (a string representing the fuel transaction ID), customerName (the name of the customer), litersPurchased (the quantity of fuel bought in liters), and pricePerLiter (the cost of one liter of the fuel).

Two classes, Petrol and Diesel, inherit from the Fuel class. The Petrol class applies a 3% discount on the total bill amount, whereas the Diesel class applies a 5% discount on the total bill amount.

Your task is to write a program that accepts exactly three fuel purchase records. Each record starts with the fuel type (either Petrol or Diesel), followed by the fuelId, customerName, litersPurchased, and pricePerLiter.

For each record, the program should calculate the total price after applying the respective discount and display the details of the purchase, including the discount rate and the final amount payable. 
## AIM:
To write a Java program using inheritance where subclasses apply different discount rates and compute the final bill amount for fuel purchases.

## ALGORITHM :
1.Start the program.

2.Define a base class Fuel with attributes:
2.1. fuelId
2.2. customerName
2.3. litersPurchased
2.4. pricePerLiter

3.Create a constructor in Fuel to initialize these attributes.

4.Define a method calculateTotal() in Fuel that returns:
litersPurchased × pricePerLiter.

5.Create subclass Petrol extending Fuel:
5.1. Override a method to apply 3% discount on the total.

6.Create subclass Diesel extending Fuel:
6.1. Override a method to apply 5% discount on the total.

In the main() method:
7.1. Loop 3 times to accept input.
7.2. Read fuel type (Petrol/Diesel).
7.3. Read fuelId, customerName, litersPurchased, pricePerLiter.
7.4. Create the corresponding object (Petrol or Diesel).
7.5. Calculate the discounted total.
7.6. Display fuel details, discount rate, and final payable amount.

8.End the program




## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Jeevansurya k
RegisterNumber: 212222040061
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
import java.text.DecimalFormat;

class Fuel {
    String fuelId, customerName;
    double litersPurchased, pricePerLiter;

    Fuel(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        this.fuelId = fuelId;
        this.customerName = customerName;
        this.litersPurchased = litersPurchased;
        this.pricePerLiter = pricePerLiter;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateTotalPrice() {
        double total = litersPurchased * pricePerLiter;
        double discountAmount = total * getDiscountRate() / 100;
        return total - discountAmount;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: General");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

class Petrol extends Fuel {
    Petrol(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        super(fuelId, customerName, litersPurchased, pricePerLiter);
    }

    @Override
    double getDiscountRate() {
        return 3.0;
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: Petrol");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

class Diesel extends Fuel {
    Diesel(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        super(fuelId, customerName, litersPurchased, pricePerLiter);
    }

    @Override
    double getDiscountRate() {
        return 5.0; 
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: Diesel");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

public class FuelStation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read until input ends (EOF)
        while (sc.hasNextLine()) {
            String type = sc.nextLine().trim();
            if (type.isEmpty()) break; // stop if blank line

            String fuelId = sc.nextLine().trim();
            String customerName = sc.nextLine().trim();
            double liters = sc.nextDouble();
            double price = sc.nextDouble();
            if (sc.hasNextLine()) sc.nextLine(); 

            Fuel fuel;
            if (type.equalsIgnoreCase("Petrol")) {
                fuel = new Petrol(fuelId, customerName, liters, price);
            } else if (type.equalsIgnoreCase("Diesel")) {
                fuel = new Diesel(fuelId, customerName, liters, price);
            } else {
                fuel = new Fuel(fuelId, customerName, liters, price);
            }

            fuel.display();
        }

        sc.close();
    }
}



```

## OUTPUT:


<img width="853" height="811" alt="image" src="https://github.com/user-attachments/assets/f236b8a3-79de-47ae-bef7-9826e45208a0" />


## RESULT:
Thus the program executed successfully.

