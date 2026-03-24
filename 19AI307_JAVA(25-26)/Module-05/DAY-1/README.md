# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

Input	Result
sample.txt
welcome
File written successfully.


## AIM:
To create a file and write text into it using FileWriter in Java.

## ALGORITHM :
1. Read the filename.
2. Read the text to write.
3. Create a FileWriter object with the filename.
4. Write the text using write().
5. Close the FileWriter.
6. Print confirmation message.






## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Sanjay T
Register Number: 212222040147
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String filename = sc.nextLine();
        String content = sc.nextLine();

        try {
            FileWriter fw = new FileWriter(filename);
            fw.write(content);
            fw.close();
            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}
```






## OUTPUT:
<img width="457" height="158" alt="image" src="https://github.com/user-attachments/assets/8d1be7e2-f7a4-4bc4-918e-49e6ec266a5d" />



## RESULT:
The program successfully writes characters to a file using FileWriter.
