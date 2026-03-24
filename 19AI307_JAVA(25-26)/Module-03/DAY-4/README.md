# Ex.No:3(D)    INTERFACE 

## QUESTION:
You’re designing a system for a food delivery app like ZomEats. Customers can choose how their food is delivered:

BikeDelivery: For orders under ₹200

CarDelivery: For orders above ₹200

DroneDelivery: For super-fast express delivery (only available on demand)

The app uses an interface called DeliveryMode which all delivery types implement.

When a customer places an order, the app selects a delivery type and shows a message about how the food will be delivered.

What Students Must Do:
Create an interface DeliveryMode with a method deliver()

Implement BikeDelivery, CarDelivery, and DroneDelivery classes

Based on amount and choice, select the correct delivery type and call deliver()

Input Format:
First line: Order amount (int)

Second line: Preferred mode (bike/car/drone)

Output Format:
Display the mode of delivery message

For example:

Input	Result
180
bike
Your food is on the way via bike delivery!
500
drone
Your express order will fly to you via drone!
250
helicopter
Invalid delivery mode.
350
car
Your food will arrive in a car with extra insulation.


## AIM:
To use interfaces and polymorphism to choose the correct delivery mode based on user input.

## ALGORITHM :
1. Read order amount.
2. Read preferred delivery mode (bike/car/drone).
3. Create an interface DeliveryMode with deliver().
4. Implement:
       - BikeDelivery → "Your food is on the way via bike delivery!"
       - CarDelivery → "Your food will arrive in a car with extra insulation."
       - DroneDelivery → "Your express order will fly to you via drone!"
5. If mode is invalid → print "Invalid delivery mode."
6. Otherwise call deliver().






## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:
```
import java.util.*;

interface DeliveryMode {
    void deliver();
}

class BikeDelivery implements DeliveryMode {
    public void deliver() {
        System.out.println("Your food is on the way via bike delivery!");
    }
}

class CarDelivery implements DeliveryMode {
    public void deliver() {
        System.out.println("Your food will arrive in a car with extra insulation.");
    }
}

class DroneDelivery implements DeliveryMode {
    public void deliver() {
        System.out.println("Your express order will fly to you via drone!");
    }
}

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int amount = Integer.parseInt(sc.nextLine());
        String mode = sc.nextLine().toLowerCase();

        DeliveryMode delivery = null;

        if (mode.equals("bike")) {
            delivery = new BikeDelivery();
        } 
        else if (mode.equals("car")) {
            delivery = new CarDelivery();
        } 
        else if (mode.equals("drone")) {
            delivery = new DroneDelivery();
        }

        if (delivery == null) {
            System.out.println("Invalid delivery mode.");
        } else {
            delivery.deliver();
        }
    }
}
```






## OUTPUT:

<img width="560" height="79" alt="image" src="https://github.com/user-attachments/assets/ea423ff4-2c3d-42c7-bf08-369b66edac39" />


## RESULT:
The program successfully demonstrates delivery mode selection using interfaces and polymorphism.
