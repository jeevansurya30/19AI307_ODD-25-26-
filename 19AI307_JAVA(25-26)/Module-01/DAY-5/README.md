# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To Write a Java program to reverse a given string.

## ALGORITHM :
1.Start the program.

2.Read the input string from the user.

3.Initialize an empty string rev = "" to store the reversed string.

4.Loop from the last character of the string to the first.

5.Append each character to rev.

6.After the loop ends, rev will contain the reversed string.

7.Display the reversed string.

8.End the program.





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by:Raghul S 
RegisterNumber:212222040128  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ReverseString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();

        String reversed = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }
        System.out.println("Reversed string: " + reversed);
    }
}
```

## OUTPUT:


<img width="818" height="355" alt="image" src="https://github.com/user-attachments/assets/1fa53923-9ed8-4c9c-beaa-9d236215680b" />


## RESULT:
Thus the program executed successfully.

