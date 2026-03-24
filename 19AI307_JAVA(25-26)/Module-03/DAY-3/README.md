# Ex.No:3(C) ABSTRACTION

## QUESTION:
In a secret intelligence facility, encrypted messages are stored as arrays of characters. Each type of agent has a different way to decode these messages. Define an abstract class Decoder with a method decodeMessage(String[] fragments).
There are two types of agents:

AlphaAgent: Extracts a meaningful string by rearranging the fragments based on even indices first, then odd indices, and then reversing the final result.

BetaAgent: Picks all fragments that start and end with the same letter, joins them with -, and removes all vowels from the resulting string.

Input Format:

First line: Integer N (number of fragments)  
Next N lines: The string fragments  
Next line: 1 for AlphaAgent, 2 for BetaAgent


Output Format:

Decoded message (string)

Explanation:

For input:

5
alpha
echo
bravo
oslo
omega
1

Rearrangement Steps for AlphaAgent:
First pick even-indexed fragments :
["alpha", "bravo", "omega"]

Then pick odd-indexed fragments :
["echo", "oslo"]

Merge them:
["alpha", "bravo", "omega", "echo", "oslo"]

Reverse this list:
["oslo", "echo", "omega", "bravo", "alpha"]

Join as a single string:
"osloechoomegabravoalpha"

Your output should be: osloechoomegabravoalpha

Rearrangement Steps for BetaAgent:

For input:

4
level
radar
agent
pop
2

Select specific fragments
Only consider fragments where:

The first character and the last character of the string are the same
(e.g., "radar" → 'r' == 'r', "agent" → 'a' != 't' → discard)

Combine with a dash
Join the selected fragments using the - symbol (hyphen).

Censor vowels
Remove all vowels (a, e, i, o, u) – both uppercase and lowercase – from the final joined string.

Your output should be: "lvl-rdr-pp"

For example:

Input	Result
5
alpha
echo
bravo
oslo
omega
1
osloechoomegabravoalpha
4
level
radar
agent
pop
2
lvl-rdr-pp


## AIM:
To implement abstraction, inheritance, and method overriding to decode encrypted message fragments differently based on agent type.

## ALGORITHM :
1. Read N → number of fragments.
2. Read N string fragments into an array.
3. Read agent type: 1 = AlphaAgent, 2 = BetaAgent.

For AlphaAgent:
    a. Take fragments at even indices.
    b. Then take fragments at odd indices.
    c. Merge both lists.
    d. Reverse the final list.
    e. Join all fragments → final decoded string.

For BetaAgent:
    a. Select fragments whose first and last characters are the same.
    b. Join them using "-" (hyphen).
    c. Remove all vowels from the combined string.
    d. Return the censored decoded string.

4. Print the decoded result.






## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class Decoder {
    abstract String decodeMessage(String[] fragments);
}

class AlphaAgent extends Decoder {
    String decodeMessage(String[] fragments) {
        ArrayList<String> even = new ArrayList<>();
        ArrayList<String> odd = new ArrayList<>();

        // Pick even and odd indexed fragments
        for (int i = 0; i < fragments.length; i++) {
            if (i % 2 == 0)
                even.add(fragments[i]);
            else
                odd.add(fragments[i]);
        }

        // Merge lists
        even.addAll(odd);

        // Reverse
        Collections.reverse(even);

        // Join into one string
        StringBuilder sb = new StringBuilder();
        for (String f : even) {
            sb.append(f);
        }

        return sb.toString();
    }
}

class BetaAgent extends Decoder {
    String decodeMessage(String[] fragments) {
        ArrayList<String> chosen = new ArrayList<>();

        // Pick fragments starting & ending with same letter
        for (String f : fragments) {
            if (f.charAt(0) == f.charAt(f.length() - 1)) {
                chosen.add(f);
            }
        }

        // Join with -
        String joined = String.join("-", chosen);

        // Remove vowels
        return joined.replaceAll("[aeiouAEIOU]", "");
    }
}

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = Integer.parseInt(sc.nextLine());
        String[] fragments = new String[n];

        for (int i = 0; i < n; i++) {
            fragments[i] = sc.nextLine();
        }

        int type = Integer.parseInt(sc.nextLine());

        Decoder agent;

        if (type == 1)
            agent = new AlphaAgent();
        else
            agent = new BetaAgent();

        System.out.println(agent.decodeMessage(fragments));
    }
}
```






## OUTPUT:
<img width="368" height="245" alt="image" src="https://github.com/user-attachments/assets/c961c50b-d88b-4a01-8b29-dc316aabb5a5" />



## RESULT:
The program successfully decodes messages using abstraction and specialized agent logic.
