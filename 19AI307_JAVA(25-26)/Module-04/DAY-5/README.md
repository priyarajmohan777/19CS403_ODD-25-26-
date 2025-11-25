# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## For example:
<img width="416" height="188" alt="image" src="https://github.com/user-attachments/assets/a8d89195-240d-496b-ba19-b6a18a3daec6" />


## AIM:
To write a Java program demonstrating the Behavior Design Pattern (Memento) to save and restore versions of an article’s content.

## ALGORITHM :
1.	Start the program.
2.	Import the java.util package for input and list handling.
3.	Create classes Article, ArticleMemento, and ArticleHistory to implement the memento mechanism.
4.	Read n versions of article content from the user and save each version.
5.	Read the restore index and retrieve the corresponding saved version.
6.	Restore the content and display the output or show an error for invalid index.
7.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: PRIYA R
RegisterNumber: 212222040124 
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

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }

    public List<ArticleMemento> getAllVersions() {
        return versions;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();

        int n = Integer.parseInt(sc.nextLine());

        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        int restoreIndex = Integer.parseInt(sc.nextLine());

        ArticleMemento m = history.getVersion(restoreIndex);
        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}
```

## OUTPUT:

<img width="730" height="517" alt="image" src="https://github.com/user-attachments/assets/39cf3455-d22b-4e9f-9189-b89b09dabefc" />

## RESULT:
Thus, the Java program implementing the Memento behavior design pattern to save and restore article versions is executed successfully.
