# TL;DR - Sorting with Collections.sort and Arrays.sort

- Collections.sort lets us sort Lists`<T>` as long as the type of things we're sorting (T) implements Comparable`<T>`

    ```java
      // assuming babies is an unsorted ArrayList<Baby>
      Collections.sort(babies);
      // babies is now sorted by the natural order of Baby!
    ```
- can do the same thing with an array of Comparable things if you use Arrays.sort

    ```java
    // assuming snails is an unsorted Snail[]
    Arrays.sort(snails);
    // snails is now snorted by the natural order of Snail!
    ```
    
- these sorts don't change the relative order of elements that return compareTo 0  