# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Print Right-Angled Triangle Star Pattern

For example:

Input	Result
3
*
* *
* * *



## AIM:
To display a right-angled triangle pattern using stars.

## ALGORITHM :
1. Read integer n.
2. For each row i from 1 to n:
       Print i stars with spaces in between.
	
## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```


## OUTPUT:

<img width="219" height="200" alt="image" src="https://github.com/user-attachments/assets/f3ac2f81-b883-40b2-aa4f-774781b99c63" />


## RESULT:
The right-angled triangle star pattern is printed successfully.

