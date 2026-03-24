# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is a treasure hunter and has reached the final chamber of the dungeon. To unlock the treasure chest, she must enter a secret 4-digit code.

A riddle appears on the wall:

"The code is hidden in the numbers you enter. Solve these puzzles to form it!"

The puzzle has 4 steps:

First digit = sum of the first two numbers

Second digit = difference between the third and fourth numbers

Third digit = product of the second and fourth numbers

Fourth digit = remainder when third number is divided by first number

Input Format:
Enter four numbers as input (integers):

<number1>
<number2>
<number3>
<number4>
Output Format:

The treasure code
The treasure code is: <digit1><digit2><digit3><digit4>

For example:

Input	Result
4
3
10
2
The treasure code is: 7862


## AIM:
To generate a 4-digit treasure code using sum, difference, product, and modulus operations on four input integers.

## ALGORITHM :
1. Read four integers: n1, n2, n3, n4.
2. Compute first digit = n1 + n2.
3. Compute second digit = n3 - n4.
4. Compute third digit = n2 * n4.
5. Compute fourth digit = n3 % n1.
6. Display the code as a single 4-digit output.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## Sourcecode.java:

       import java.util.Scanner;
       
       public class Sourcecode {
           public static void main(String[] args) {
               Scanner sc = new Scanner(System.in);

        int n1 = sc.nextInt();
        int n2 = sc.nextInt();
        int n3 = sc.nextInt();
        int n4 = sc.nextInt();

        int d1 = n1 + n2;
        int d2 = n3 - n4;
        int d3 = n2 * n4;
        int d4 = n3 % n1;

        System.out.println("The treasure code is: " + d1 + "" + d2 + "" + d3 + "" + d4);
    }
}

## OUTPUT:
<img width="401" height="174" alt="image" src="https://github.com/user-attachments/assets/c120352b-8b15-4159-b289-58fe07652de9" />

## RESULT:
Thus, the treasure code is successfully generated based on the given logic.

