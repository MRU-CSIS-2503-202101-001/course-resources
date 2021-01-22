# TL;DR - More generics

- you can show dot-files (files with a dot in front of them) in the Eclipse Package Explorer if you go to the three-dot button, then go `Filters` and uncheck the `.* resource` checkox
- if you open up the `.classpath` file in your project directory and change the `true` in the following to `false`:

    ```xml
    name="ignore_optional_problems" value="true" 
    ```
  then we'll get useful warning about using generics unsafely - but at the cost of getting some duplicate warnings showing up (since PMD and the compiler will beak off about a lot of the same things)
- if you want to create a generic class that uses only types that implement a certain interface, then we (confusingly) use the **extends** keyword like so:

    ```java
    public class Stomach<T extends Digestible> {}
    ```

- yes, you can have these types implement multiple interfaces:

    ```java
    public class Stomach<T extends Digestible, Comparable<T>> {}
    ```