Java provides several ways to handle input and output, including reading user input, displaying results, and working with files.
### **Key Concepts:**

**Commands and Arguments:**  
    Java programs can accept user-defined input through **command-line arguments** and execute various commands based on them.
```
public class Example {
    public static void main(String[] args) {
        System.out.println("First argument: " + args[0]);
    }
}
```


**Usage:**
```
java Example Hello
Output: First argument: Hello
```


**Standard Output:**  
The default way to display information in Java is through `System.out.println()`, which prints text to the console.

```
System.out.println("Hello, World!");
```

**Formatted Output:**

Java provides `System.out.printf()` and `String.format()` to control the formatting of printed text.

- For Number Formatting `%d`
```
int a=10000;
System.out.printf("%,d%n",a);
```
#### Output
`10,000`

- Formatting Decimal Numbers `%f`
```java
// declaring double
double a = 3.14159265359;

// Printing Double Value with
// different Formatting
System.out.printf("%f\n", a);
System.out.printf("%5.3f\n", a);
System.out.printf("%5.2f\n", a);
```
#### Output
```
3.141593
3.142
 3.14
```
- For Boolean Formatting `‘%b’ or ‘%B’`
```java
int a = 10;
Boolean b = true, c = false;
Integer d = null;

System.out.printf("%b\n", a);
System.out.printf("%B\n", b);
System.out.printf("%b\n", c);
System.out.printf("%B\n", d);
```
#### Output
```
true
TRUE
false
FALSE
```
- For Char Formatting ` ‘%c’ and ‘%C’`
```java
char c = 'a';

System.out.printf("%c\n", c);

// Converting into Uppercase
System.out.printf("%C\n", c);
```
#### Output
```
a
A
```

- For String Formatting `‘%s’ and ‘%S’`
```java
String str = "algorithm";

// Formatting from lowercase to
// Uppercase
System.out.printf("%s \n", str);
System.out.printf("%S \n", str);

str = "AR";
// Vice-versa not possible
System.out.printf("%S \n", str);
System.out.printf("%s \n", str);
```
#### Output
```
algorithm 
ALGORITHM 
AR 
AR 
```
- For Date and Time Formatting
```java
Date time = new Date();

System.out.printf("Current Time: %tT\n", time);

// Another Method with all of them Hour
// minutes and seconds seperated
System.out.printf("Hours: %tH  Minutes: %tM Seconds: %tS\n", time, time, time);

// Another Method to print the time
// Followed by am/pm , time in milliseconds
// nanoseconds and time-zone offset
System.out.printf("%1$tH:%1$tM:%1$tS %1$tp %1$tL %1$tN %1$tz %n", time);
```
#### Output
```
Current Time: 11:32:36
Hours: 11  Minutes: 32 Seconds: 36
11:32:36 am 198 198000000 +0000 
```
**String format()**
```java
String str1 = String.format("%d", 101);          // Integer value  
String str2 = String.format("%s", "A R Rahman"); // String value  
String str3 = String.format("%f", 101.00);       // Float value  
String str4 = String.format("%x", 101);          // Hexadecimal value  
String str5 = String.format("%c", 'c');          // Char value
System.out.println(str1);  
System.out.println(str2);  
System.out.println(str3);  
System.out.println(str4);  
System.out.println(str5);  
```
#### Output
```
101
A R Rahman
101.000000
65
c
```
**Standard Input:**  
Java uses `Scanner` to read user input from the keyboard.

```
import java.util.Scanner;

public class InputExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        System.out.println("Hello, " + name);
    }
}
```

**Redirection and Piping:**

Java programs can read input from a file or send output to a file using **redirection** in the terminal.
```
java Program < input.txt > output.txt
```

This redirects `input.txt` as the input and saves the output to `output.txt`.

**Input and Output from a File:**

Java provides `Scanner` for reading files and `PrintWriter` for writing to files.

```
import java.io.*;

public class FileIO {
    public static void main(String[] args) throws IOException {
        // Reading from a file
        Scanner scanner = new Scanner(new File("input.txt"));
        while (scanner.hasNextLine()) {
            System.out.println(scanner.nextLine());
        }
        scanner.close();

        // Writing to a file
        PrintWriter writer = new PrintWriter("output.txt");
        writer.println("Hello, file!");
        writer.close();
    }
}
```

