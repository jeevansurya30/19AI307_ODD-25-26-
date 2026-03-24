# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it says "Skipped".

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.

## AIM:
To write a Java program that simulates the behavior of a magical elevator by checking floor numbers using conditional statements and printing the appropriate message.

## ALGORITHM :
1.Start the program.

2.Read the floor number as input.

3.Check if the floor number is divisible by both 3 and 5:

If true, print "Skipped".

4.Else, check if the floor number is divisible only by 3:

If true, print "Beware!".

5.Else, check if the floor number is divisible only by 5:

If true, print "Blessings!".

6.Otherwise:

Print "Floor {number}" where number is the floor entered.

7.End the program.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Raghul S
RegisterNumber: 212222040128 
*/
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        int n = input.nextInt();
        if((n%3==0)&&(n%5==0)) System.out.println("Skipped");
        else if((n%3==0)) System.out.println("Beware!");
        else if(n%5==0) System.out.println("Blessings!");
        else System.out.println("Floor "+n);
    }
}
```



## OUTPUT:

<img width="650" height="384" alt="image" src="https://github.com/user-attachments/assets/e70caa4b-be6c-4c68-a789-ebd84b1e8f6a" />


## RESULT:
Thus the program executed successfully.
