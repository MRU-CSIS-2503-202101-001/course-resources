# TL;DR - The Basics of Optionals

- Optional<T> is like a "box" that is either empty or holds an object of type T
- to make them, you use the static methods `empty` and `of`:

    ```java
      import java.util.Optional; // don't forget to import!
      
      Optional<Integer> foo = Optional.empty(); // this Optional is empty
      Optional<String> bar = Optional.of("ham"); // this Optinal has the String "ham" inside it
    ```
- you can ask an Optional object if it is empty and then react to that:

    ```java
    // assume we have an Optional variable called opt
    if (opt.isEmpty()) {
      // do something
    } else {
      // do something else
    }
    ```
    
- conversely, you can ask an Optional object if it is NOT empty and then react to that:

    ```java
    // assume we have an Optional variable called opt
    if (opt.isPresent()) {
      // do something
    } else {
      // do something else
    }
    ```

- if you want to get a value out of an Optional (you should check if something is there first!), then you can:

    ```java
    // assume we have an Optional<String> variable called opt
    if (opt.isPresent()) {
      String thingInside = opt.get();
      // do something with thingInside
    }
    ```