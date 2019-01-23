+++
title = "SRP (Single Responsibility Principle)"
description = "SRP (Single Responsibility Principle)"
chapter = true
weight = 1
pre = "<b>1. </b>"
+++

## SRP (Single Responsibility Principle)
---
![srp](srp.jpg)

### Bad:
```java
package srp.bad;

public class Book {
    private String bookName;

    private String authorName;

    private String content;

    public Book(String bookName, String authorName, String content) {
        this.bookName = bookName;
        this.authorName = authorName;
        this.content = content;
    }

    public String getBookName() {
        return bookName;
    }

    public void setBookName(String bookName) {
        this.bookName = bookName;
    }

    public String getAuthorName() {
        return authorName;
    }

    public void setAuthorName(String authorName) {
        this.authorName = authorName;
    }

    public String getContent() {
        return content;
    }

    public void setContent(String content) {
        this.content = content;
    }

    public void show(IDevice device) {
        String text = String.format("Name: %s, author: %s, content: %s", this.bookName, this.authorName, this.content);
        device.display(text);
    }
}
```


```java
package srp.bad;

interface IDevice
{
    void display(String data);
}
```

```java
package srp.bad;

public class WindowsConsole implements IDevice {
    public void display(String text){
        System.out.println(text);
    }
}
```

```java
package srp.bad;

public class Main {
    public static void main(String[] args) {
        Book book = new Book("Book Name", "Author Name", "text text text");
        IDevice device = new WindowsConsole();
        book.show(device);
    }
}
```

### Good:
```java
package srp.good;

public class Book {
    private String bookName;

    private String authorName;

    private String content;

    public Book(String bookName, String authorName, String content) {
        this.bookName = bookName;
        this.authorName = authorName;
        this.content = content;
    }

    public String getBookName() {
        return bookName;
    }

    public void setBookName(String bookName) {
        this.bookName = bookName;
    }

    public String getAuthorName() {
        return authorName;
    }

    public void setAuthorName(String authorName) {
        this.authorName = authorName;
    }

    public String getContent() {
        return content;
    }

    public void setContent(String content) {
        this.content = content;
    }
}
```

```java
package srp.bad;

interface IDevice
{
    void display(String data);
}
```

```java
package srp.bad;

public class WindowsConsole implements IDevice {
    public void display(String text){
        System.out.println(text);
    }
}
```

```java
package srp.good;

public class BookDisplay {
    public void show(Book book, IDevice device) {
        String text = String.format("Name: %s, author: %s, content: %s", book.getBookName(), book.getAuthorName(), book.getContent());
        device.display(text);
    }
}
```

```java
package srp.bad;

public class Main {
    public static void main(String[] args) {
        Book book = new Book("Book Name", "Author Name", "text text text");
        IDevice device = new WindowsConsole();

        BookDisplay bookDisplay = new BookDisplay();
        bookDisplay.show(book, device);
    }
}
```

---
#### Read More:
- ?
