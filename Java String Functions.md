## Java String Functions with Definitions, Syntax, and Examples

### String Creation and Input

1. **String Creation**

   * **Definition**: Creating a string object in Java.
   * **Syntax**:

     ```java
     String s1 = "Hello";
     String s2 = new String("World");
     ```

2. **String Input** (Using Scanner)

   * **Definition**: Getting a string from user input.
   * **Syntax**:

     ```java
     Scanner sc = new Scanner(System.in);
     String input = sc.nextLine();
     ```

---

### String Methods

3. **length()** - Returns the length of the string

   * `s.length()`

4. **charAt(index)** - Returns the character at the given index

   * `s.charAt(1)`

5. **substring(beginIndex, endIndex)** - Returns a substring

   * `s.substring(1, 4)`

6. **contains(CharSequence)** - Checks if string contains sequence

   * `s.contains("ll")`

7. **equals(String)** - Compares strings (case-sensitive)

   * `s.equals("Hello")`

8. **equalsIgnoreCase(String)** - Compares strings ignoring case

   * `s.equalsIgnoreCase("hello")`

9. **toLowerCase()** - Converts to lowercase

   * `s.toLowerCase()`

10. **toUpperCase()** - Converts to uppercase

    * `s.toUpperCase()`

11. **replace(char, char)** - Replaces characters

    * `s.replace('l', 'x')`

12. **trim()** - Removes leading and trailing spaces

    * `s.trim()`

13. **indexOf(char)** - Returns index of first occurrence

    * `s.indexOf('e')`

14. **lastIndexOf(char)** - Last occurrence of character

    * `s.lastIndexOf('l')`

15. **split(regex)** - Splits string by regex

    * `s.split(" ")`

16. **startsWith(prefix)** - Checks if starts with

    * `s.startsWith("He")`

17. **endsWith(suffix)** - Checks if ends with

    * `s.endsWith("lo")`

18. **isEmpty()** - Checks if empty

    * `s.isEmpty()`

19. **compareTo(String)** - Lexicographical comparison

    * `s.compareTo("Hello")`

20. **valueOf(int)** - Converts to string

    * `String.valueOf(100)`

---

### Full Java Program with All Examples

```java
import java.util.*;

public class StringFunctions {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // String creation
        String s1 = "Hello";
        String s2 = new String("World");

        // Input string
        System.out.print("Enter a string: ");
        String input = sc.nextLine();
        System.out.println("You entered: " + input); // Example: Aggu

        System.out.println("Length: " + s1.length()); // 5
        System.out.println("charAt(1): " + s1.charAt(1)); // 'e'
        System.out.println("substring(1,4): " + s1.substring(1, 4)); // 'ell'
        System.out.println("contains('ll'): " + s1.contains("ll")); // true
        System.out.println("equals('Hello'): " + s1.equals("Hello")); // true
        System.out.println("equalsIgnoreCase('hello'): " + s1.equalsIgnoreCase("hello")); // true
        System.out.println("toLowerCase(): " + s1.toLowerCase()); // 'hello'
        System.out.println("toUpperCase(): " + s1.toUpperCase()); // 'HELLO'
        System.out.println("replace('l','x'): " + s1.replace('l', 'x')); // 'Hexxo'
        System.out.println("trim(): " + "  Hello  ".trim()); // 'Hello'
        System.out.println("indexOf('e'): " + s1.indexOf('e')); // 1
        System.out.println("lastIndexOf('l'): " + s1.lastIndexOf('l')); // 3

        // split()
        String[] words = "Java is fun".split(" ");
        System.out.println("split(' '): " + Arrays.toString(words)); // [Java, is, fun]

        System.out.println("startsWith('He'): " + s1.startsWith("He")); // true
        System.out.println("endsWith('lo'): " + s1.endsWith("lo")); // true
        System.out.println("isEmpty(): " + "".isEmpty()); // true
        System.out.println("compareTo('Hello'): " + s1.compareTo("Hello")); // 0
        System.out.println("valueOf(100): " + String.valueOf(100)); // "100"

        sc.close();
    }
}
```

Compile and run the program with:

```bash
javac StringFunctions.java
java StringFunctions
```
