# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

Input:

Two lines: a and b values

Output:

a = <swapped_a>

b = <swapped_b>

For example:

Input	Result
5
10
a = 10
b = 5


## AIM:
To read two integers, use a synchronized block to safely swap them, and display the swapped results.

## ALGORITHM :
1. Read integers a and b.
2. Create an Object lock for synchronization.
3. Use synchronized(lock):
       temp = a
       a = b
       b = temp
4. Print swapped values.






## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
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

        int a = sc.nextInt();
        int b = sc.nextInt();

        Object lock = new Object();

        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}
```





## OUTPUT:

<img width="208" height="154" alt="image" src="https://github.com/user-attachments/assets/abea5bd6-8742-4055-9b59-d9850447321d" />



## RESULT:
The program successfully swaps two numbers using a synchronized block.
