# Task7.Library

May 10, 2024

Deadline: May 23 (inclusive)

## Task 7

Create three classes

* `Book` with fields `author`, `title` and `body` (of type `String`);
* `Shelf` with fields `id` (`String`) and `books` – array of Books;
* `Library` with only one field `shelves` – array of shelves.

All fields must be `private`. Provide necessary constructors and getters.

In the class `Library` add a method `countAuthor` which counts (and returns as an `int`) the number of books in the library written by author whose name (`String`) is passed as an argument to the method. In a separate class define function `main`

download ObjsII1Lib.java

```java
public static void main (String[] args) {
    Shelf shelf1 = new Shelf("Shelf1",
      new Book[]{
          new Book("Babel","Odessa Tales","babelode"),
          new Book("Joyce","Ulisses","joyceuli")
      });
    Shelf shelf2 = new Shelf("Shelf2",
      new Book[]{
        new Book("Mann","Dr Faustus","mannfau"),
        new Book("Babel","Red Cavalry","babelred")
      });
Library lib = new Library(
      new Shelf[]{shelf1,shelf2});
System.out.println("# of books by this author: " +
                        lib.countAuthor("Babel"));
}
```

which, for this example, should print

```
No of book by this author: 2
```

## Solution

[Replit](https://replit.com/@piecucci/Task7Library?v=1)

```java
class Book {
    private String author;
    private String title;
    private String body;

    public Book(String author, String title, String body) {
        this.author = author;
        this.title = title;
        this.body = body;
    }

    public String getAuthor() {
        return author;
    }

    public String getTitle() {
        return title;
    }

    public String getBody() {
        return body;
    }
} 
```

```java
class Library {
    private Shelf[] shelves;

    public Library(Shelf[] shelves) {
        this.shelves = shelves;
    }

    public int countAuthor(String authorName) {
        int count = 0;
        for (Shelf shelf : shelves) {
            for (Book book : shelf.getBooks()) {
                if (book.getAuthor().equals(authorName)) {
                    count++;
                }
            }
        }
        return count;
    }
}
```

```java
class Shelf {
    private String id;
    private Book[] books;

    public Shelf(String id, Book[] books) {
        this.id = id;
        this.books = books;
    }

    public String getId() {
        return id;
    }

    public Book[] getBooks() {
        return books;
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        Shelf shelf1 = new Shelf("Shelf1",
                new Book[]{
                        new Book("Babel", "Odessa Tales", "babelode"),
                        new Book("Joyce", "Ulisses", "joyceuli")
                });
        Shelf shelf2 = new Shelf("Shelf2",
                new Book[]{
                        new Book("Mann", "Dr Faustus", "mannfau"),
                        new Book("Babel", "Red Cavalry", "babelred")
                });
        Library lib = new Library(new Shelf[]{shelf1, shelf2});
        System.out.println("# of books by this author: " + lib.countAuthor("Mann"));
    }
}
```

[Contents](https://github.com/Java-PJATK/00.Contents)
