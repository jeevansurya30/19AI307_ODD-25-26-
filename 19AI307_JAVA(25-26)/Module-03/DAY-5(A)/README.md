# Ex.No:3(E) INNER CLASS

## QUESTION:
Write an enum VehicleType (CAR, BIKE, BUS) with a constructor that takes number of wheels. Print wheel count for each.

## AIM:
To Write an enum VehicleType (CAR, BIKE, BUS) with a constructor that takes number of wheels. Print wheel count for each.

## ALGORITHM :
1.Start the program.

2.Create an enum VehicleType with constants CAR, BIKE, BUS.

3.Add a constructor to the enum that accepts the number of wheels.

4.Store the wheel count in a private instance variable.

5.Provide a method to return the wheel count.

6.In the main() method, print each vehicle type and its wheel count.

7.End the program.




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: RAGHUL S
RegisterNumber: 212222040128 
*/
```

## SOURCE CODE:


```

import java.util.Scanner;

enum VehicleType {
    CAR(4),
    BIKE(2),
    BUS(6);

    private int wheels;

    VehicleType(int wheels) {
        this.wheels = wheels;
    }

    public int getWheels() {
        return wheels;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine().trim().toUpperCase(); // handle lowercase

        try {
            VehicleType v = VehicleType.valueOf(input);
            System.out.println(v + " has " + v.getWheels() + " wheels.");
        } catch (IllegalArgumentException e) {
            System.out.println("Invalid vehicle type entered.");
        }
    }
}

```

## OUTPUT:


<img width="843" height="378" alt="image" src="https://github.com/user-attachments/assets/a6b2c55c-151a-4df3-a12f-9a1759d11a18" />


## RESULT:
Thus,the program executed successfully.

