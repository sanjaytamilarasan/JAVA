# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java program to demonstrate a parameterized constructor.

Input    Result
Manoj
53
Employee Name: Manoj
Employee ID: 53

## AIM:
To create a class with a parameterized constructor and display the values passed to it.

## ALGORITHM :
1. Create a class Employee.
2. Declare variables name and id.
3. Create a parameterized constructor that assigns values to these variables.
4. In main():
       - Read name and id.
       - Create an Employee object using the constructor.
       - Print the values.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Employee {
    String name;
    int id;

    Employee(String name, int id) {
        this.name = name;
        this.id = id;
    }

    void display() {
        System.out.println("Employee Name: " + name);
        System.out.println("Employee ID: " + id);
    }
}

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int id = sc.nextInt();

        Employee e = new Employee(name, id);
        e.display();
    }
}
```





## OUTPUT:
<img width="458" height="207" alt="image" src="https://github.com/user-attachments/assets/1ce07974-edcf-434b-b5e0-1340b735070a" />



## RESULT:
The program successfully demonstrates a parameterized constructor.
