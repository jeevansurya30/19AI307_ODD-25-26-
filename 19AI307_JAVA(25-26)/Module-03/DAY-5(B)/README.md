# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## AIM:
To Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## ALGORITHM :
1.Start the program.

2.Read a numeric string value from the user.

3.Convert the string to an integer using Integer.parseInt().

4.Read another integer value from the user.

5.Add the converted integer and the second integer.

6.Print the result.

7.End the program.



## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Jeevansurya k
RegisterNumber: 212222040061
*/
```

## SOURCE CODE:

```

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str1 = sc.nextLine();           // first string input
        String str2 = sc.nextLine();           // second string input

        int num1 = Integer.parseInt(str1);     // convert to integer
        int num2 = Integer.parseInt(str2);     // convert to integer

        System.out.println("Sum = " + (num1 + num2));
    }
}

```
## OUTPUT:

<img width="502" height="444" alt="image" src="https://github.com/user-attachments/assets/3d8aa8d3-345c-4e3d-80c6-5f8ee10a46f2" />



## RESULT:
Thus ,the program executed successfully.

