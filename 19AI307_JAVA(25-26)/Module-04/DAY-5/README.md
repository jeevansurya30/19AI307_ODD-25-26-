# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create a ChatRoom class (mediator) and two users (colleagues) who send and receive messages through it. No direct communication allowed. (Mediator Pattern)

## AIM:

To implement the Mediator design pattern in Java by building a ChatRoom mediator that facilitates message exchange between User objects.

## ALGORITHM :
1.Start the program.

2.Define a ChatRoom interface (mediator) with a method to send messages.

3.Implement ConcreteChatRoom which stores registered users and routes messages to the intended recipient(s).

4.Define a User class (colleague) that has a name and reference to the ChatRoom. Include send() and receive() methods.

5.In main(), create a ChatRoom instance and two User instances. Register users with the chat room.

6.Have users send messages via the chat room; the chat room forwards the messages to recipients.

7.Print messages as users receive them.

8.End the program.




## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Jeevansurya k
RegisterNumber: 212222040061
*/
```

## SOURCE CODE:

```
import java.util.*;

class ChatRoom {
    private Map<String, User> users = new HashMap<>();

    public void registerUser(User user) {
        users.put(user.getName(), user);
    }

    public void sendMessage(String from, String to, String message) {
        User receiver = users.get(to);
        if (receiver != null) {
            receiver.receive(from, message);
        } else {
            System.out.println("User " + to + " not found");
        }
    }
}

class User {
    private String name;
    private ChatRoom chatRoom;

    public User(String name, ChatRoom chatRoom) {
        this.name = name;
        this.chatRoom = chatRoom;
        chatRoom.registerUser(this);
    }

    public String getName() {
        return name;
    }

    public void send(String to, String message) {
        chatRoom.sendMessage(name, to, message);
    }

    public void receive(String from, String message) {
        System.out.println(from + " to " + name + ": " + message);
    }
}

public class ChatApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        ChatRoom room = new ChatRoom();
        User user1 = new User(sc.nextLine(), room); 
        User user2 = new User(sc.nextLine(), room); 

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String sender = sc.nextLine();
            String receiver = sc.nextLine();
            String message = sc.nextLine();

            if (sender.equals(user1.getName())) {
                user1.send(receiver, message);
            } else if (sender.equals(user2.getName())) {
                user2.send(receiver, message);
            } else {
                System.out.println("Unknown sender");
            }
        }

        sc.close();
    }
}



```

## OUTPUT:


<img width="1145" height="754" alt="image" src="https://github.com/user-attachments/assets/6e46abbf-4061-4e32-bfc8-9d740cac5e50" />


## RESULT:

Thus,The program executed successfully.
