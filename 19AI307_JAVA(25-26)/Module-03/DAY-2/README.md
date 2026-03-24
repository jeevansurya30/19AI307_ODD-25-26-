# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a base class Animal (Animal Family) with a method called Sound(). Create two subclasses Bird and Cat. Override the Sound() method in each subclass to make a specific sound for each animal.

## AIM:
To Write a Java program to create a base class Animal (Animal Family) with a method called Sound(). Create two subclasses Bird and Cat. Override the Sound() method in each subclass to make a specific sound for each animal.

## ALGORITHM :
1.Start the program.

2.Create a base class Animal with a method named Sound() that prints a generic message.

3.Create a subclass Bird extending Animal:
3.1. Override Sound() to print the sound of a bird.

4.Create a subclass Cat extending Animal:
4.1. Override Sound() to print the sound of a cat.

5.In the main() method:
5.1. Create an object of Bird and call its Sound() method.
5.2. Create an object of Cat and call its Sound() method.

6.Display the respective animal sounds.

7.End of the program


## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Jeevansurya k
RegisterNumber:212222040061
*/
```

## SOURCE CODE:
```

import java.util.Scanner;

class Animal {
    void Sound() {
        System.out.println("Animal makes a sound");
    }
}

class Bird extends Animal {
    @Override
    void Sound() {
        System.out.println("Bird chirps");
    }
}

class Cat extends Animal {
    @Override
    void Sound() {
        System.out.println("Cat meows");
    }
}

public class AnimalSound {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine().trim().toLowerCase();

        Animal animal;

        if (input.equals("bird")) {
            animal = new Bird();
        } else if (input.equals("cat")) {
            animal = new Cat();
        } else {
            // default animal sound for other inputs
            animal = new Animal();
        }

        animal.Sound();
        sc.close();
    }
}


```


## OUTPUT:


<img width="586" height="368" alt="image" src="https://github.com/user-attachments/assets/c17feb4a-a69a-49b7-8e71-3b6205a0d8a5" />


## RESULT:
Thus the program executed successfully.
