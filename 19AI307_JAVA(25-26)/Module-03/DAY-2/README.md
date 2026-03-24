# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to perform the addition of two numbers using method overloading. The program should contain two overloaded methods named sum():

One that takes two integers and returns their sum.

One that takes two double values and returns their sum.

For example:

Input	Result
8
9
17
5.5
8.5
14.0

## AIM:
To implement method overloading by defining two sum() methods: one for integers and one for double values.

## ALGORITHM :
1. Read two integers.
2. Call sum(int, int) → returns integer sum.
3. Read two double values.
4. Call sum(double, double) → returns double sum.
5. Print both results.


## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Sourcecode {

    // Overloaded method for integers
    static int sum(int a, int b) {
        return a + b;
    }

    // Overloaded method for doubles
    static double sum(double a, double b) {
        return a + b;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int x = sc.nextInt();
        int y = sc.nextInt();
        System.out.println(sum(x, y));

        double p = sc.nextDouble();
        double q = sc.nextDouble();
        System.out.println(sum(p, q));
    }
}
```





## OUTPUT:

<img width="191" height="154" alt="image" src="https://github.com/user-attachments/assets/dc8e1472-a146-4114-b08d-c3cf91a331ad" />


## RESULT:
The program successfully demonstrates method overloading to add integers and doubles.
