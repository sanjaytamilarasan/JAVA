# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
At the annual "KrackerJack Karnival", there was a newest attraction ever in the City, the "Hanging Bridge". Visitors will be able to walk 200ft on the bridge, hanging around 50ft above the ground, and enjoy a wide-angle view of the breathtaking greenery.


The Hanging Bridge was inaugurated successfully in co-ordination with the Event Manager Rahul. There is a limit on the maximum number of people on the bridge and Rahul has to now ensure the count of people on the bridge currently should not exceed the limit. He then approximately estimated that C adults and D kids who came to the show, were on the hanging bridge. He also noticed that there are L legs of the people touching the bridge.


Rahul knows that kids love to ride on the adults and they might ride on the adults, and their legs won't touch the ground and hence he would miss counting their legs. Also Rahul knew that the adults would be strong enough to ride at max two kids on their back.
Rahul is now wondering whether he counted the legs properly or not. Specifically, he is wondering is there some possibility of his counting being correct. Please help Rahul in finding it.
 
Input :
Number of the adults,

Number of the kids 

Number of legs of people counted by Rahul, respectively.

Output :
"yes" or "no" according to the situation.


For example:

Input	Result
1 1 4
yes
2 4 16
no


## AIM:
To check whether the counted number of legs can be correct considering adults may carry up to two kids, making those kids’ legs not touch the bridge.

## ALGORITHM :
1. Read adults A, kids K, and legs L.
2. Minimum legs = adults*2  (all kids riding)
3. Maximum legs = (adults + kids)*2  (everyone on ground)
4. If L is between minimum and maximum legs:
       print "yes"
   Else:
       print "no"

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
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

        int A = sc.nextInt();  // adults
        int K = sc.nextInt();  // kids
        int L = sc.nextInt();  // legs counted

        int maxKidsRiding = Math.min(K, 2 * A);
        int kidsOnGround = K - maxKidsRiding;

        int minLegs = (A * 2) + (kidsOnGround * 2);
        int maxLegs = (A + K) * 2;

        if (L >= minLegs && L <= maxLegs)
            System.out.println("yes");
        else
            System.out.println("no");
    }
}
```

## OUTPUT:

<img width="190" height="86" alt="image" src="https://github.com/user-attachments/assets/37a33ada-6cec-4fb0-853b-01c01a2c3ac5" />


## RESULT:
The program correctly determines whether the leg count is possible.

