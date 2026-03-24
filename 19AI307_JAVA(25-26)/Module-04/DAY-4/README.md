# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types.

## AIM:
To implement the Abstract Factory design pattern to produce theme-specific UI components (Button and Checkbox) for dark and light themes and display the created component types.

## ALGORITHM :
1.Start the program.

2.Define Button and Checkbox interfaces with a method to return/display their type (e.g., getType() or render()).

3.Define an abstract factory interface UIFactory with methods createButton() and createCheckbox().

4.Implement concrete products: DarkButton, LightButton, DarkCheckbox, LightCheckbox.

5.Implement concrete factories: DarkFactory and LightFactory that return the corresponding products.

6.In main(), read user input for the theme (dark or light).

7.Instantiate the appropriate factory and create the Button and Checkbox.

8.Display the types of the created components.

9.End the program.




## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Jeevansurya k
RegisterNumber:  212222040061
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface Button {
    void render();
}

interface Checkbox {
    void render();
}
class DarkButton implements Button {
    public void render() {
        System.out.println("Dark Button created");
    }
}

class LightButton implements Button {
    public void render() {
        System.out.println("Light Button created");
    }
}
class DarkCheckbox implements Checkbox {
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

class LightCheckbox implements Checkbox {
    public void render() {
        System.out.println("Light Checkbox created");
    }
}
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}
class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }

    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }

    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        UIFactory factory;

        if (theme.equals("dark")) factory = new DarkThemeFactory();
        else if (theme.equals("light")) factory = new LightThemeFactory();
        else {
            System.out.println("Invalid theme");
            return;
        }

        factory.createButton().render();
        factory.createCheckbox().render();
    }
}




```

## OUTPUT:


<img width="725" height="433" alt="image" src="https://github.com/user-attachments/assets/a5c12da1-24d3-4a7f-b52e-a2fb177c1822" />


## RESULT:

Thus,the program executed successfully.
