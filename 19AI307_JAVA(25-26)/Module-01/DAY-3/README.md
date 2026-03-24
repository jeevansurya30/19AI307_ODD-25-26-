# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to calculate the factorial of a number using a for loop. The factorial of n is the product of all positive integers less than or equal to n.

## AIM:
To write a Java program that calculates the factorial of a given number using a for loop.

## ALGORITHM :
1.Start the program.

2.Read an integer n from the user.

3.Initialize a variable fact = 1.

4.Use a for loop that runs from 1 to n.

5.Multiply fact by the loop variable at each iteration.

6.After the loop ends, fact will contain the factorial of the number.

7.Print the final factorial value.

8.End the program.


## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by:Jeevansurya k
RegisterNumber: 212222040061
*/
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        int n = input.nextInt();
        int fact=1;
        for(int i=1;i<=n;i++)
        {
            fact=fact*i;
        }
        System.out.println("Factorial of "+n+" is: "+fact);
    }
    
}
```



## OUTPUT:
<img width="809" height="354" alt="image" src="https://github.com/user-attachments/assets/7c7fc79c-e650-4cc2-8e51-8aa169dd693c" />



## RESULT:
Thus the Program Executed Successfully.

