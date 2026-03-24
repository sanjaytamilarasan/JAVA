# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

import java.util.Scanner;

class BankAccount {
    // Private instance variables
    private String accountNumber;
    private double balance;

    // Getter and Setter for accountNumber
    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    // Getter and Setter for balance
    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

## AIM:
To implement encapsulation using private variables and public getters/setters in Java.

## ALGORITHM :
1. Create a class BankAccount.
2. Declare private variables: accountNumber (String), balance (double).
3. Provide public getter and setter for accountNumber.
4. Provide public getter and setter for balance.
5. In main():
       - Create an object of BankAccount.
       - Read account number and balance.
       - Set them using setters.
       - Print them using getters.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class BankAccount {
    private String accountNumber;
    private double balance;

    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        BankAccount b = new BankAccount();

        String acc = sc.nextLine();
        double bal = sc.nextDouble();

        b.setAccountNumber(acc);
        b.setBalance(bal);

        System.out.println("Account Number: " + b.getAccountNumber());
        System.out.println("Balance: " + b.getBalance());
    }
}
```






## OUTPUT:
<img width="472" height="194" alt="image" src="https://github.com/user-attachments/assets/059e0776-e8ee-4fa7-b6e1-ac8d0915155c" />



## RESULT:
The program successfully uses getters and setters to access private variables.
