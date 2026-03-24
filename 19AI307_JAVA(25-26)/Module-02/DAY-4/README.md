# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java program to demonstrate a parameterized constructor.

## AIM:
To Write a Java program to demonstrate a parameterized constructor.

## ALGORITHM :
1.Start the program.

2.Create a class (e.g., Student).

3.Declare instance variables (e.g., name, age).

4.Define a parameterized constructor that accepts values for the variables.

5.Assign the constructor parameters to the instance variables.

6.Create an object in the main() method and pass values to the constructor.

7.Display the initialized values.

8.End the program.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Jeevansurya k
RegisterNumber: 212222040061
*/
```

## SOURCE CODE:

```
import java.util.*;
class Employee{
    private String name;
    private int id;
    private Employee(String name,int id){
        this.name=name;
        this.id=id;
    }
    public static Employee createem(String name,int id){
        return new Employee(name,id);
    }
    public void display(){
        System.out.println("Employee Name: "+name);
        System.out.println("Employee ID: "+id);
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        int id=sc.nextInt();
        Employee emp=Employee.createem(name,id);
        emp.display();
    }
}
```


## OUTPUT:


<img width="717" height="421" alt="image" src="https://github.com/user-attachments/assets/5836c3aa-788f-4ca3-870d-2a3979e42e8d" />


## RESULT:
Thus , the program executed successfully
