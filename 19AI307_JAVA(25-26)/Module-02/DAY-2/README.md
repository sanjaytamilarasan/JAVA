# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

For example:

Input	Result
5
125


## AIM:
To compute the cube of a number using one method calling another.

## ALGORITHM :
1. Read integer x.
2. Define square(x) → returns x*x.
3. Define cube(x) → returns x * square(x).
4. Print cube(x).





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Sourcecode {
    
    static int square(int x) {
        return x * x;
    }

    static int cube(int x) {
        return x * square(x);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.println(cube(n));
    }
}
```





## OUTPUT:

<img width="188" height="65" alt="image" src="https://github.com/user-attachments/assets/820f1352-ee53-43b2-ba8b-1372cb17ba76" />


## RESULT:
The cube is successfully calculated using the square() method.
