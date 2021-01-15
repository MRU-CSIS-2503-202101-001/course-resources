# Reading Numbers from Console

## In a Nutshell

Almost everyone's been bitten by this: you have some code that reads in a number (int, double) from the keyboard, followed by some code that reads in a String...and when you run the code, the program never gives the user a chance to read the String - it seems to read in the number and just "skip" the String reading part! WTF?!!?

This video explains what's going on and talks about 2 ways - one which I suggest you use - to fix it. It then explains why I like the one I do.

## The Screencast

It's available [[here]](https://youtu.be/Bj8IBxAmODY) [24:49]

## TL;DR

- When you use `nextInt` or `nextDouble`, the Scanner you're using will wind up "stopping" on a newline character. If you then do a `nextLine`, **only** that newline character is read, causing `nextLine` to return an empty String!
- Fix one: do an additional `nextLine` immediately after your `nextInt`:

    ```java
    int someNum = kbd.nextInt();
    kbd.nextLine(); // eats the offending newline and tosses it out
    ```
- Fix two: read the user input as a String using `nextLine` and then turn it into an int (or double) using `Integer.parseInt`:

    ```java
    String someNumAsText = kbd.nextLine();
    int someNum = Integer.parseInt(someNumAsText);
    // if you need a double, use Double.parseDouble(someText)
    ```

- The main benefit of the second method is that it lets you validate the user input easily with regular expressions.