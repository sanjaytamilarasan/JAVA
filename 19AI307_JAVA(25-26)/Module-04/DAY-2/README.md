# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

Key Hint (Hidden in Story):
Only one control tower object should exist.

Every flight contacting it should register its name.

You should log the order of flights that contacted the tower.

Input Format:
First line: Integer n – number of incoming flights

Next n lines: Each line contains the flight name.

Output Format:
For each flight, print:

[FlightName] registered with Radar Control Tower. Total Flights: [count]

For example:

Input	Result
3
AI101
BA202
EK303
AI101 registered with Radar Control Tower. Total Flights: 1
BA202 registered with Radar Control Tower. Total Flights: 2
EK303 registered with Radar Control Tower. Total Flights: 3


## AIM:
To implement the Singleton design pattern ensuring only one Radar Control Tower object exists, and all flights register through the same instance.

## ALGORITHM :
1. Create a Singleton class RadarControlTower:
       - Private static instance variable.
       - Private constructor.
       - Public static getInstance() method returning the single instance.
       - Method registerFlight(String name) that increments count and prints log.

2. In main():
       - Read number of flights n.
       - For each flight:
             Read flight name.
             Call RadarControlTower.getInstance().
             Call registerFlight(flightName).






## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class RadarControlTower {

    private static RadarControlTower instance = null;
    private int flightCount = 0;

    // Private constructor
    private RadarControlTower() {}

    // Singleton access method
    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    // Register a flight
    public void registerFlight(String flightName) {
        flightCount++;
        System.out.println(flightName + " registered with Radar Control Tower. Total Flights: " + flightCount);
    }
}

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            tower.registerFlight(flight);
        }
    }
}
```





## OUTPUT:

<img width="559" height="107" alt="image" src="https://github.com/user-attachments/assets/63324d84-0518-45bb-9cc3-3ffa06c7d818" />


## RESULT:
The program successfully implements the Singleton pattern ensuring all flights use the same Radar Control Tower instance.
