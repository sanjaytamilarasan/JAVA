# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

For example:

Input	Result
3
Initial draft
Revised content
Final article version
2
Final article version


## AIM:
To implement the Memento Design Pattern to save and restore different versions of an article.

## ALGORITHM :
1. Create an Article class that stores the current content.
2. Create a Memento class to store a snapshot of the content.
3. Create a CareTaker class to hold a list of mementos.
4. For each new content:
       - Save it as a memento in CareTaker.
5. After saving all versions, read the version number to restore.
6. Retrieve the corresponding memento and restore the content.
7. Print the restored content.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Sanjay T
Register Number:  212222040147
*/
```

## SOURCE CODE:
```
import java.util.*;

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }
    public String getContent() {
        return content;
    }

    // Create memento
    public Memento saveToMemento() {
        return new Memento(content);
    }

    // Restore from memento
    public void restoreFromMemento(Memento m) {
        this.content = m.getSavedContent();
    }
}

class Memento {
    private final String content;

    public Memento(String content) {
        this.content = content;
    }

    public String getSavedContent() {
        return content;
    }
}

class CareTaker {
    private ArrayList<Memento> versions = new ArrayList<>();

    public void addMemento(Memento m) {
        versions.add(m);
    }

    public Memento getMemento(int index) {
        return versions.get(index);
    }
}

class Sourcecode {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();
        sc.nextLine();

        Article article = new Article();
        CareTaker caretaker = new CareTaker();

        // Saving versions
        for (int i = 0; i < n; i++) {
            String text = sc.nextLine();
            article.setContent(text);
            caretaker.addMemento(article.saveToMemento());
        }

        int versionToRestore = sc.nextInt();
        versionToRestore--; // Convert to 0-based index

        article.restoreFromMemento(caretaker.getMemento(versionToRestore));

        System.out.println(article.getContent());
    }
}
```






## OUTPUT:
<img width="398" height="284" alt="image" src="https://github.com/user-attachments/assets/938f0204-c7de-489a-9ec5-221e7eb6cbc2" />



## RESULT:
The program successfully saves multiple article versions and restores any selected version using the Memento pattern.

