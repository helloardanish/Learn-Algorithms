A String is a sequence of characters ([char values](https://www.cs.cmu.edu/~pattis/15-1XX/common/handouts/ascii.html)) enclosed in **double quotes (" ")**. Strings are used to store and manipulate text. The data type String is a Java data type but it is not a primitive type. Java provides the **`String`** class, which is part of the **`java.lang`** package.

It is a fundamental data type that almost every Java program uses.

#### **Declaring and Creating a String**

You can create a string in Java in two ways:
#### **a) Using String Literals (Stored in String Pool)**

```java
String str1 = "Hello, Java!";
```
- Stored in the **String Pool** (part of Java Heap Memory).
- If another string with the same value exists, Java will reuse it (memory optimization).

#### **b) Using the `new` Keyword (Stored in Heap Memory)**

```java
String str2 = new String("Hello, Java!");
```

- Creates a **new object** in the heap memory (not in the String Pool).
- Even if a string with the same value exists, a new object is created.

---

### **Important Properties of Strings in Java**

- **Strings are Immutable**: Once created, they cannot be changed.
- **Stored in String Pool**: Java optimizes memory by reusing existing strings.
- **String Class is Final**: It cannot be extended.

Example of immutability:
```java
String s = "Hello";
s.concat(" World"); // This does not change "s", it creates a new string.
System.out.println(s); // Output: Hello
```
To modify the string, you need to **reassign** it:
```java
s = s.concat(" World");
System.out.println(s); // Output: Hello World
```
---


### **Common String Methods**

Java provides many built-in methods in the `String` class.

#### **a) Finding Length of a String**

```java
String s = "Java Programming";
System.out.println(s.length()); // Output: 16
```

#### b) Converting to Upper/Lower Case

```java
String s = "Java";
System.out.println(s.toUpperCase()); // Output: JAVA
System.out.println(s.toLowerCase()); // Output: java
```

#### c) Checking if Strings are Equal

```java
String s1 = "Java";
String s2 = "java";

System.out.println(s1.equals(s2)); // false (case-sensitive)
System.out.println(s1.equalsIgnoreCase(s2)); // true (ignores case)
```
#### d) Extracting a Substring

```java
String s = "Hello, World!";
System.out.println(s.substring(7)); // Output: World!
System.out.println(s.substring(0, 5)); // Output: Hello
```
#### e) Checking if a String Contains a Substring
```java
String s = "Learning Java is fun";
System.out.println(s.contains("Java")); // true
System.out.println(s.contains("Python")); // false
```
#### f) Replacing Characters or Words
```java
String s = "I love Java";
System.out.println(s.replace("Java", "Python")); // Output: I love Python
```
#### g) Splitting a String
```java
String sentence = "Apple, Banana, Mango";
String[] fruits = sentence.split(", ");
for (String fruit : fruits) {
    System.out.println(fruit);
}
// Output:
// Apple
// Banana
// Mango
```
#### h) Removing Whitespace (`trim()` method)
```java
String s = "  Hello Java  ";
System.out.println(s.trim()); // Output: "Hello Java" (removes leading and trailing spaces)
```

---
### **String Concatenation (Joining Strings)**

Java has a built-in concatenation operator (+) for String like the built-in operators that it has for primitive types. The result of concatenating two String values is a single String value, the first string followed by the second.

#### a) Using `+` Operator
```java
String firstName = "John";
String lastName = "Doe";
String fullName = firstName + " " + lastName;
System.out.println(fullName); // Output: John Doe
```

#### b) Using `concat()` Method
```java
String s1 = "Hello";
String s2 = "World";
String s3 = s1.concat(" ").concat(s2);
System.out.println(s3); // Output: Hello World
```

---

### String Comparison (`==` vs `equals()`)
#### Using `==` (Compares Object References)
```java
String s1 = "Hello";
String s2 = "Hello";
System.out.println(s1 == s2); // true (because both point to the same object in String Pool)

String s3 = new String("Hello");
System.out.println(s1 == s3); // false (different memory locations)
```
#### Using `equals()` (Compares Actual Content)
```java
System.out.println(s1.equals(s3)); // true (because values are the same)
```

---

### **Mutable Alternatives: `StringBuilder` and `StringBuffer`**

Since `String` is immutable, modifying it creates a **new object**, which can be inefficient.  
For performance reasons, use **StringBuilder** or **StringBuffer**.

#### **Using `StringBuilder` (Faster, Not Thread-Safe)**

```java
StringBuilder sb = new StringBuilder("Hello");
sb.append(" World");
System.out.println(sb); // Output: Hello World
```

#### Using `StringBuffer` (Thread-Safe, Slower)
```java
StringBuffer sb = new StringBuffer("Hello");
sb.append(" World");
System.out.println(sb); // Output: Hello World
```

---
