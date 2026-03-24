# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to concatenate two strings.

Input	Result
hello
world
Concatenated string: helloworld


## AIM:
To read two strings and join them into a single concatenated string.

## ALGORITHM :
1. Read the first string.
2. Read the second string.
3. Concatenate both strings.
4. Print the result.






## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
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

        String s1 = sc.nextLine();
        String s2 = sc.nextLine();

        String result = s1 + s2;

        System.out.println("Concatenated string: " + result);
    }
}
```






## OUTPUT:

<img width="479" height="155" alt="image" src="https://github.com/user-attachments/assets/c45548f3-e784-41d6-949b-95ea1114001e" />


## RESULT:
The program successfully concatenates the two strings.
