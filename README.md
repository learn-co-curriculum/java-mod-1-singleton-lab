# Singleton Lab

## Learning Goals

- Use the singleton pattern

## Introduction

We'll be creating a logging library. In our (simplified) case, logging requires
access to the console of the computer we're logging the output on.

## Instructions

We want our logger instance to be a singleton because we want to be able to
output the line numbers with each output statement, and we want those line
numbers to be incremented across the entire system regardless of what class is
printing information out.

Hints:

- Call your class `Logger`.
- Everywhere you need access to the "logger", you will use the
  `Logger.getInstance()` method to get an instance of the Logger and then use
  whatever methods the logger provides to output statements to the console.
- Implement a `log()` method that takes a `String` parameter and output the line
  number before outputting the message passed in.

Your output from using your logger should look something like this:

```plainttext
1::Sample output line 1
2::Second line of sample output
```

Note: The `Main` class will use the `Logger` class as such:

```java
public class Main {
    public static void main(String[] args) {
        Logger.getInstance().log("Sample output line 1");
        Logger.getInstance().log("Second line of sample output");
    }
}
```
