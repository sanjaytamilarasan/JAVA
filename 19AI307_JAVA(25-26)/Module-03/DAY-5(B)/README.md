# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes. 

Input	Result
29
29 is a prime number.


## AIM:
To read a number using an Integer wrapper class and determine if it is prime.

## ALGORITHM :
1. Read input number n.
2. Convert it into an Integer object.
3. If n <= 1 → not prime.
4. Loop from 2 to sqrt(n):
       If n % i == 0 → not prime.
5. If no divisor found → prime.
6. Print result.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Sourcecode {

    static boolean isPrime(Integer n) {
        if (n <= 1)
            return false;

        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0)
                return false;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Integer num = sc.nextInt();

        if (isPrime(num))
            System.out.println(num + " is a prime number.");
        else
            System.out.println(num + " is not a prime number.");
    }
}
```






## OUTPUT:

<img width="396" height="115" alt="image" src="https://github.com/user-attachments/assets/7f147ad7-0e39-4782-92a9-90f0c19c8cdc" />


## RESULT:
The program successfully checks if a number is prime using wrapper classes.
