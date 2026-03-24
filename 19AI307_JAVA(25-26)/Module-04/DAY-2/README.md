# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
You are designing a microservices-based system where multiple services like AuthService, UserService, OrderService, etc., need to log important system events.

To maintain centralized logging (and not have separate loggers for each service), the system uses a Singleton Logger.

Each service logs messages with its name and log level.

Log levels can be: INFO, WARNING, or ERROR.

Every log message is stored in order of occurrence and the logger prints the entire log history each time a new message is added.

🧩 Concepts Student Must Apply:
Implement a Singleton class (Logger) that holds logs.

Maintain logs as a list of strings.

Each log message must be formatted as:
"[Service] [LEVEL]: message"

Print full log history after each new log.

Input Format:
First line: Integer n – number of logs

Next n lines: Each contains:
[ServiceName] [Level] [Message]
(The message has no spaces.)

Output Format:
After each log, print:

[Service] [LEVEL]: message
Current Logs:
1. log1
2. log2

## AIM:
To write a Java program that demonstrates the Singleton design pattern by centralizing logs from multiple microservices, storing them in a list, and displaying full log history after each entry.

## ALGORITHM :
1.Start the program.

2.,Create a Singleton Logger class with a private constructor and a static getInstance() method.

3.Store logs in a list of strings inside the logger.

4.Write a method addLog(service, level, message) that formats and stores the log.

5.After storing, print the latest log and the complete log history.

6.In main(), read the number of logs.

7.For each log input, call the logger's method to add the log.

8.End the program.




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by:Jeevansurya k
RegisterNumber: 212222040061
*/
```

## SOURCE CODE:

```
import java.util.*;

class Logger {
    private static Logger instance;
    private List<String> logs;

    private Logger() {
        logs = new ArrayList<>();
    }

    public static Logger getInstance() {
        if (instance == null) {
            instance = new Logger();
        }
        return instance;
    }

    public void addLog(String service, String level, String message) {
        String log = service + " " + level + ": " + message;
        logs.add(log);
        System.out.println(log);
        System.out.println("Current Logs:");
        for (int i = 0; i < logs.size(); i++) {
            System.out.println((i + 1) + ". " + logs.get(i));
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");
            String service = input[0];
            String level = input[1];
            String message = input[2];

            Logger logger = Logger.getInstance();
            logger.addLog(service, level, message);
            System.out.println();
        }
    }
}



```

## OUTPUT:


<img width="1240" height="786" alt="image" src="https://github.com/user-attachments/assets/835122d0-d490-4c00-9a07-0a88bcd28dda" />


## RESULT:

Thus, the program executed successfully . 
