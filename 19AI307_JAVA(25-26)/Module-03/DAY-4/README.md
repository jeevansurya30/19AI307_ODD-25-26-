# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.

## AIM:
To You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.



## ALGORITHM :
1.Start the program.

2.Create an interface WeatherBot with a method predict(int temperature).

3.Create a class SunBot that implements the interface and returns "HOT" or "MODERATE" based on temperature.

4.Create a class RainBot that implements the interface and returns "COLD" or "WARM" based on temperature.

5.In the main() method, read temperature and bot type from the user.

6.Based on bot type, create the appropriate bot object.

7.Call the predict() method and print the result.

8.End the program.




## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by:Jeevansurya k 
RegisterNumber:  212222040061
*/
```

## SOURCE CODE:

```
import java.util.*;

// Common interface
interface WeatherBot {
    String predict(int temperature);
}

// SunBot class
class SunBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature > 30)
            return "HOT";
        else
            return "MODERATE";
    }
}

// RainBot class
class RainBot implements WeatherBot {
    public String predict(int temperature) {
        if (temperature < 20)
            return "COLD";
        else
            return "WARM";
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();
        int type = sc.nextInt();

        WeatherBot bot;
        if (type == 1)
            bot = new SunBot();
        else
            bot = new RainBot();

        System.out.println(bot.predict(temperature));
    }
}


```



## OUTPUT:


<img width="452" height="287" alt="image" src="https://github.com/user-attachments/assets/6f870831-1fbe-4d29-abe6-93509f037c11" />


## RESULT:
Thus, the program executed successsfully.
