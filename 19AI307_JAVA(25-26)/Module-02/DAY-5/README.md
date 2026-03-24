# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Write a method that accepts a string and returns whether it contains only lowercase letters or not.

## AIM:
To Write a method that accepts a string and returns whether it contains only lowercase letters or not.

## ALGORITHM :
1.Start the program.

2.Read the input string from the user.

3.Create a method isLowercase(String str) that:
3.1. Loops through each character in the string.
3.2. Checks if the character lies between 'a' and 'z'.
3.3. If any character is outside this range, return false.
3.4. If all characters are lowercase, return true.

4.In the main() method, call isLowercase() with the input string.

5.Display whether the string contains only lowercase letters or not.

6.End the program.



## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by:RAGHUL S 
RegisterNumber: 212222040128
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class StringCheck {

    boolean isAllLowercase(String str) {
        // Check if string matches only lowercase letters a-z
        return str.matches("[a-z]+");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine();

        StringCheck obj = new StringCheck();
        System.out.println(obj.isAllLowercase(input));
    }
}
```






## OUTPUT:


<img width="491" height="350" alt="image" src="https://github.com/user-attachments/assets/a791a211-8f55-4c4d-bb08-721ee9dc6295" />


## RESULT:
Thus the program executed successfully.
