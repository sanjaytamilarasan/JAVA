# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to simulate inter-thread communication using PipedInputStream and PipedOutputStream, where one thread writes data (input taken from the user) and another thread reads and displays the data.

Input	Result
welcome java
ReaderThread received: welcome java


## AIM:
To demonstrate communication between two threads using piped streams in Java.

## ALGORITHM :
1. Create PipedInputStream and PipedOutputStream.
2. Connect the streams.
3. Create WriterThread:
       - Reads input from user.
       - Writes data into PipedOutputStream.
4. Create ReaderThread:
       - Reads data from PipedInputStream.
       - Displays the received message.
5. Start both threads.






## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Sanjay T
Register Number: 212222040147
*/
```

## SOURCE CODE:

```
import java.io.*;
import java.util.Scanner;

class WriterThread extends Thread {
    private PipedOutputStream pos;

    WriterThread(PipedOutputStream pos) {
        this.pos = pos;
    }

    public void run() {
        try {
            Scanner sc = new Scanner(System.in);
            String message = sc.nextLine();
            pos.write(message.getBytes());
            pos.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

class ReaderThread extends Thread {
    private PipedInputStream pis;

    ReaderThread(PipedInputStream pis) {
        this.pis = pis;
    }

    public void run() {
        try {
            byte[] buffer = new byte[1000];
            int len = pis.read(buffer);
            String received = new String(buffer, 0, len);
            System.out.println("ReaderThread received: " + received);
            pis.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

class Sourcecode {
    public static void main(String[] args) throws IOException {
        PipedOutputStream pos = new PipedOutputStream();
        PipedInputStream pis = new PipedInputStream(pos);

        WriterThread writer = new WriterThread(pos);
        ReaderThread reader = new ReaderThread(pis);

        writer.start();
        reader.start();
    }
}
```





## OUTPUT:

<img width="459" height="119" alt="image" src="https://github.com/user-attachments/assets/6aa20034-3b67-4ed1-895a-4a703ba3ca1d" />



## RESULT:
The program successfully demonstrates inter-thread communication using PipedInputStream and PipedOutputStream.
