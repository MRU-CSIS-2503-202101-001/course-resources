# TL;DR - Pre-built compareTo and multi-field compareTo

- if **our** compareTo uses fields that already have a compareTo built-in, we should use those!
  
    ```java
      // assume Baby has a LocalDateTime field dob
      int compareTo(Baby other) {
        return this.dob.compareTo(other.dob);
      }
    ```
    
- if you want to sort alphabetically, don't forget to use `compareToIgnoreCase`:  

    ```java
    int compareTo(Baby other) {
      return this.name.compareToIgnoreCase(other.name);
    }
    ```
- reverse ordering means just switching the `this` and `other` around:

    ```java
    // compare in reverse alphabetic order on name
    int compareTo(Baby other) {
      return other.name.compareToIgnoreCase(this.name);
    }
    ```
- if coding up a multi-field natural ordering, typically have this kind of pattern:

    ```java
    int compareTo(T t) {
      int primaryCompareResult = // some comparison
      if (primaryCompareResult != 0) {
        return primaryCompareResult;
      } else {
        return // secondary comparison
      }
    }
    ```
- you can use the ternary operator to clean up the if/else a bit
- you can do 3 levels (or more) of comparison