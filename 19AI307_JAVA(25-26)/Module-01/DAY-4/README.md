# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to count the number of positive, negative, and zero elements in an array

For example:

Input	Result
5
1
-2
0
-3
4
Positive count: 2
Negative count: 2
Zero count: 1


## AIM:
To read an array of integers and count how many are positive, negative, and zero.

## ALGORITHM :
1. Read n → number of elements.
2. Loop n times:
       Read each element.
       If element > 0 → increase positive count.
       Else if element < 0 → increase negative count.
       Else → increase zero count.
3. Print the three counts.






## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        int pos = 0, neg = 0, zero = 0;

        for (int i = 0; i < n; i++) {
            int x = sc.nextInt();

            if (x > 0) pos++;
            else if (x < 0) neg++;
            else zero++;
        }

        System.out.println("Positive count: " + pos);
        System.out.println("Negative count: " + neg);
        System.out.println("Zero count: " + zero);
    }
}



```


## OUTPUT:

<img width="303" height="314" alt="image" src="https://github.com/user-attachments/assets/2553738f-c17d-4eed-ae7a-871ed330060b" />


## RESULT:
The program correctly counts positive, negative, and zero elements in the array.

