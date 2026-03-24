# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:
To Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## ALGORITHM :
1.Start the program.

2.Create a class named Person.

3.Declare private instance variables:

String name

int age

String country

4.Write public setter methods to set the values of the variables.

5.Write public getter methods to return the values of the variables.

6.In the main() method:

Create an object of the Person class.

Use setter methods to assign values.

Use getter methods to display the values.

7.End the program.


## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Jeevansurya k
RegisterNumber:212222040061 
*/
```

## SOURCE CODE:

```
import java.util.*;
class Person{
    private String name;
    private int age;
    private String country;
    public String getName()
    {
        return name;
    }
    public void setName(String name)
    {
        this.name=name;
    }
    public int getAge()
    {
        return age;
    }
    public void setAge(int age)
    {
        this.age=age;
    }
    public String getCountry(){
        return country;
    }
    public void setCountry(String country)
    {
        this.country=country;
    }
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        Person ob=new Person();
        System.out.println("Person 1");
        ob.setName(sc.nextLine());
        ob.setAge(sc.nextInt());
        sc.nextLine();
        ob.setCountry(sc.nextLine());
        System.out.println("Name: "+ob.getName());
        System.out.println("Age: "+ob.getAge());
        System.out.println("Country: "+ob.getCountry());
        
    }
}
```




## OUTPUT:

<img width="854" height="543" alt="image" src="https://github.com/user-attachments/assets/5f6bc83b-5ff3-4c53-9070-a52298911aee" />



## RESULT:

Thus the porgram executed successfully.
