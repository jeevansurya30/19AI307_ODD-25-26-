# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.
## AIM:
To write a Java program that reads array elements, calculates their sum, and finds their average.

## ALGORITHM :
1.Start the program.

2.Read the size of the array (n) from the user.

3.Declare an array of size n.

4.Use a loop to input all array elements.

5.Initialize sum = 0.

6.Traverse the array using a loop and add each element to sum.

7.Compute the average

8.Print the average value.

9.End the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Jeevansurya k
RegisterNumber:  212222040061
*/
```

## SOURCE CODE:


```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int[] arr=new int[n];
        int sum=0;
        for(int i=0;i<n;i++)
        {
            arr[i]=sc.nextInt();
        }
        for(int i=0;i<n;i++)
        {
            sum+=arr[i];
        }
        float avg=(float)sum/n;
        System.out.printf("The average of elements is %.2f",avg);
    }
}
```





## OUTPUT:


<img width="898" height="564" alt="image" src="https://github.com/user-attachments/assets/bea04420-fa77-49a6-a571-8659164d85fa" />



## RESULT:
Thus , The program executed successfully.


