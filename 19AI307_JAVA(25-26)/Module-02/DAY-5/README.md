# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Write a method that accepts a string and returns whether it contains only lowercase letters or not.

 

For example:

Input	Result
saveetha
true


## AIM:
To read a string and determine if all characters are lowercase.

## ALGORITHM :
1. Read the input string.
2. Loop through each character:
       If any character is not lowercase → return false.
3. If loop finishes → return true.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Sourcecode {

    static boolean isLowercase(String s) {
        for (int i = 0; i < s.length(); i++) {
            if (!Character.isLowerCase(s.charAt(i))) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String input = sc.nextLine();
        System.out.println(isLowercase(input));
    }
}
```





## OUTPUT:
<img width="211" height="115" alt="image" src="https://github.com/user-attachments/assets/2393cab8-6830-4b26-adae-2dd394f439bf" />



## RESULT:
The program correctly checks whether the string contains only lowercase letters.
