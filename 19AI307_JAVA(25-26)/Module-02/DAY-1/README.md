# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Define a class Teacher with the following attributes:

name (String)

subject (String)

experience (int, in years)

Create an object of the class and display the teacher details.

## AIM:
To write a Java program that defines a class Teacher with attributes name, subject, and experience, and displays the details using an object.

## ALGORITHM :
1.Start the program.

2.Define a class Teacher with attributes: name, subject, and experience.

3.Create a constructor to initialize these attributes.

4.Create a method to display the teacher details.

5.In the main method:

   Create an object of the Teacher class.

  Display the teacher’s details using the display method.

6.End the program.


## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Jeevansurya k
RegisterNumber: 212222040061 
*/
```

## SOURCE CODE:

```
import java.util.*;
class Teacher 
{
String name;
String subject;
int experience;
void printMessage()
{
System.out.println("Mr. "+name+" teaches "+subject+" and has "+experience+" years experience.");
}
}

public class Main
{
public static void main(String args[])
{
Scanner input=new Scanner(System.in);
Teacher obj1 = new Teacher();
obj1.name=input.nextLine();
obj1.subject=input.nextLine();
obj1.experience=input.nextInt();
obj1.printMessage();
}
}
```

## OUTPUT:


<img width="1214" height="505" alt="image" src="https://github.com/user-attachments/assets/36a15d5d-934a-4eec-ad43-0d664e048542" />
## RESULT
Thus, The program executed successfully.

## RESULT:

