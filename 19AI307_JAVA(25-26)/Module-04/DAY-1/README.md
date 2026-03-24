# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To You wrote a program that stores some input strings into a String array and prints each string in uppercase.


## ALGORITHM :
1.Start the program.

2.Create a String array and store input values.

3.Loop through each element of the array.

4.Check if the element is not null before calling toUpperCase().

5.If it is not null, convert it to uppercase and print it.

6.If it is null, skip it or print a warning message.

7.End the program.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
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
        String input = sc.nextLine(); // read a single string input
        
        // Check for null or empty input
        if (input == null || input.equals("null")) {
            System.out.println("Null element");
        } else {
            System.out.println(input.toUpperCase());
        }

        sc.close();
    }
}




```

## OUTPUT:


<img width="579" height="378" alt="image" src="https://github.com/user-attachments/assets/61e2de37-8640-4878-8b93-9e7929bb9f28" />


## RESULT:
Thus,the program executed successfully . 

