# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Define a class Teacher with attributes: name (String), subject (String), and experience (int, years). 

import java.util.Scanner;
class Teacher {
    String name;
    String subject;
    int experience;

    void printMessage() {
        // Your Code Here
    }
}
class prog {
    public static void main(String[] args) {
       // Your Code Here
    }
}

For example:

Input	Result
John
Mathematics
10
Mr. John teaches Mathematics and has 10 years experience.


## AIM:
To create a Teacher class and print the teacher’s information using a method.

## ALGORITHM :
1. Create a Teacher class with:
       - name (String)
       - subject (String)
       - experience (int)
2. Define printMessage() to display the formatted output.
3. In main():
       - Read name, subject, and experience.
       - Create Teacher object.
       - Call printMessage().





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Sanjay T
Register Number:  212222040147 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Teacher {
    String name;
    String subject;
    int experience;

    void printMessage() {
        System.out.println("Mr. " + name + " teaches " + subject + " and has " + experience + " years experience.");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Teacher t = new Teacher();

        t.name = sc.nextLine();
        t.subject = sc.nextLine();
        t.experience = sc.nextInt();

        t.printMessage();
    }
}
```





## OUTPUT:

<img width="561" height="200" alt="image" src="https://github.com/user-attachments/assets/27429fe7-0588-493e-9296-8291c308c9a9" />



## RESULT:
The program successfully prints the teacher's details.
