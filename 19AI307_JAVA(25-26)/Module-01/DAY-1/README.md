# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:1


## AIM:
To write a Java program that takes Lovely’s age and score as input and evaluates six relational expressions using relational operators, displaying whether each condition is true or false.


## ALGORITHM :

1.	Start the program.

2.Create a Scanner object to read user input.

3.Read the first integer input as age.

4.Read the second integer input as score.

5.Evaluate the following relational expressions:

age == 18

score != 100

score > 70

score < 70

age >= 18

age <= 25

6.Print the result (true or false) for each expression in the required format.

7.End the program.




## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Raghul S
RegisterNumber: 212222040128
*/
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner input = new Scanner(System.in);
        int age = input.nextInt();
        int score = input.nextInt();
        
        System.out.println("Age == 18: " + (age == 18));
        System.out.println("Score != 100: " + (score != 100));
        System.out.println("Score > 70: " + (score > 70));
        System.out.println("Score < 70: " + (score < 70));
        System.out.println("Age >= 18: " + (age >= 18));
        System.out.println("Age <= 25: " + (age <= 25));
    }
}

```


## OUTPUT:

<img width="787" height="484" alt="image" src="https://github.com/user-attachments/assets/571fbc60-6e0b-4fee-bac2-21053e0b0483" />


## RESULT:
Thus, the program executed successfully.
