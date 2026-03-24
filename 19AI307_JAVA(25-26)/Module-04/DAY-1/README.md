# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?



## AIM:
To avoid NullPointerException by checking if an array element is null before applying .toUpperCase().

## ALGORITHM :
1. Read strings into a String array.
2. Loop through each element.
3. Before calling toUpperCase():
       Check if the element != null.
4. If not null → print element.toUpperCase().
5. If null → skip or handle accordingly.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        sc.nextLine();

        String[] arr = new String[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextLine();
        }

        for (int i = 0; i < n; i++) {
            if (arr[i] != null) {        // IMPORTANT check
                System.out.println(arr[i].toUpperCase());
            } else {
                System.out.println("Null value found, skipping.");
            }
        }
    }
}
```





## OUTPUT:
<img width="288" height="115" alt="image" src="https://github.com/user-attachments/assets/d80e1539-f8f4-4beb-af65-1aaca2b9cde2" />



## RESULT:
The program avoids NullPointerException by checking for null before using .toUpperCase().
