# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.

Note : Read the threadname from the User

Set the Priority as 2.

For example:

Input	Result
NewThread
Priority of Thread: 2
Name of Thread: NewThread
Thread[NewThread,2,main]


## AIM:
To read a thread name from the user, set it to the current thread, assign priority 2, and display thread details.

## ALGORITHM :
1. Read thread name from user.
2. Get current thread using Thread.currentThread().
3. Set the thread name.
4. Set thread priority to 2.
5. Print the priority.
6. Print the thread name.
7. Print the thread object (which displays full thread info).





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Sanjay T
Register Number: 212222040147
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread t = Thread.currentThread();

        t.setName(threadName);
        t.setPriority(2);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}
```





## OUTPUT:

<img width="408" height="92" alt="image" src="https://github.com/user-attachments/assets/d64d12d9-ccff-4e36-91c9-2d31fe61a9a8" />



## RESULT:
The program successfully sets and displays the name and priority of the current thread.
