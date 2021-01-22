# TL;DR - An Alternate Way to compare and compareTo

- we can use the very useful static methods available in the `Comparator` class to create **declarative** (as opposed to **imperative**) code (https://www.freecodecamp.org/news/imperative-vs-declarative-programming-difference/)
- need to have some getters on the fields you want to involve with creating your Comparator
- basic form is like this:

    ```java
    Comparator<Baby> comp = Comparator.comparing(Baby::getWeight);
    ```
    
    _Note the weird `::` syntax_
    
- reversing things is easy:

    ```java
    Comparator<Baby> comp = Comparator.comparing(Baby::getWeight).reversed();
    ```

- if you want to do an alphabetic, it's a bit more work:

    ```java
    Comparator<Baby> comp = Comparator.comparing(Baby::getName, String.CASE_INSENSITIVE_ORDER); // standard alphabetic
    
    Comparator<Baby> comp = Comparator.comparing(Baby::getName, String.CASE_INSENSITIVE_ORDER).reversed(); // reversed alphabetic
    ```
    
- you can chain these together to do multi-field sorts:

    ```java
    Comparator<Baby> comp = 
      Comparator.comparing(Baby::getWeight).thenComparing(Baby::getAge);
    ```

- if you want to reverse one thing in a chain, you need to be fancy:

    ```java
    Comparator<Baby> comp = 
      Comparator.comparing(Baby::getWeight, Comparator.reverseOrder()).thenComparing(Baby::getAge);
    ```

- wanna feed an alphabetic into a chain? a bit more work:

    ```java
    Comparator<Baby> alphaNameComparator = Comparator.comparing(Baby::getName, String.CASE_INSENSITIVE_ORDER).reversed();
    
    Comparator<Baby> comparator = 
      Comparator.comparing(Baby::getWeight, Comparator.reverseOrder()).thenComparing(Baby::getAge)
      .thenComparing(alphaNameComparator);
    ```