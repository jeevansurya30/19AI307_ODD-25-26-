# Ex.No:2(B) METHODS

## QUESTION:
rite a class with one static method and one non-static method.

When staticMethod() is called → print "I am static"

When nonStaticMethod() is called → print "I am non-static"
Call both from the main() method.

## AIM:
To write a Java program that demonstrates the difference between static and non-static methods and calls both from the main method.

## ALGORITHM :
1.Start the program.

2.Create a class named Demo.

3.Inside the class, define:

A static method staticMethod() that prints "I am static".

A non-static method nonStaticMethod() that prints "I am non-static".

4.In the main() method:

Call the static method using the class name.

Create an object of the class.

Use the object to call the non-static method.

5.Display the output.

6.End the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: RAGHUL S
RegisterNumber: 212222040128  
*/
```

## SOURCE CODE:

```
import java.util.*;
public class Main
{
public static void main(String args[])
{
call obj1 = new call();
obj1.staticMethod();
obj1.nonStaticMethod();
}
}
class call
{
void staticMethod()
{
System.out.println("I am static");
}
void nonStaticMethod()
{
System.out.println("I am non-static");
}
}
```



## OUTPUT:

<img width="734" height="287" alt="image" src="https://github.com/user-attachments/assets/e5d5dc6b-ab3b-4a27-ae41-f984c3fe7768" />



## RESULT:
Thus , the program executed successfully.
