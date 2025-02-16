
## Looping in Java allows executing a block of code multiple times until a condition is met.
```
There are three main types of loops:
For Loop – Used when the number of iterations is known beforehand.
While Loop – Executes the loop as long as the condition remains true.
Do-While Loop – Similar to while but ensures at least one execution before checking the condition.
Loops help in reducing code repetition, making programs efficient and readable. Nested loops allow loops inside another loop for complex iterations.

`````
### 1. Check whether a number is positive or negative  
```java   
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        if (n > 0) {
            System.out.println("Positive");
        } else if (n < 0) {
            System.out.println("Negative");
        } else {
            System.out.println("Zero");
        }
    }
}
```


```
5
Positive
```

---

### 2. Check whether a number is even or odd  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        if (n % 2 == 0) {
            System.out.println("Even");
        } else {
            System.out.println("Odd");
        }
    }
}
```

**Input:**  
```
7
```
**Output:**  
```
Odd
```

---

### 3. Check whether a number is divisible by 3 and 5  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        if (n % 3 == 0 && n % 5 == 0) {
            System.out.println("Divisible by 3 and 5");
        } else {
            System.out.println("Not divisible by 3 and 5");
        }
    }
}
```

**Input:**  
```
15
```
**Output:**  
```
Divisible by 3 and 5
```

---

### 4. Find the largest of three numbers  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        int c = s.nextInt();
        
        int max = (a > b) ? ((a > c) ? a : c) : ((b > c) ? b : c);
        System.out.println(max);
    }
}
```

**Input:**  
```
10 20 15
```
**Output:**  
```
20
```

---

### 5. Check whether a number is a prime number  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        boolean isPrime = true;

        if (n <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i * i <= n; i++) {
                if (n % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        System.out.println(isPrime ? "Prime" : "Not Prime");
    }
}
```

**Input:**  
```
17
```
**Output:**  
```
Prime
```

---

### 6. Check whether a year is a leap year  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int year = s.nextInt();
        
        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
            System.out.println("Leap Year");
        } else {
            System.out.println("Not a Leap Year");
        }
    }
}
```

**Input:**  
```
2024
```
**Output:**  
```
Leap Year
```

---

### 7. Find the greatest of four numbers  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        int c = s.nextInt();
        int d = s.nextInt();
        
        int max = Math.max(Math.max(a, b), Math.max(c, d));
        System.out.println(max);
    }
}
```

**Input:**  
```
12 45 23 78
```
**Output:**  
```
78
```

---

### 8. Check if a number is a palindrome  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int temp = n, rev = 0;
        
        while (temp > 0) {
            rev = rev * 10 + temp % 10;
            temp /= 10;
        }
        
        System.out.println(n == rev ? "Palindrome" : "Not a Palindrome");
    }
}
```

**Input:**  
```
121
```
**Output:**  
```
Palindrome
```

---

### 9. Check whether a character is a vowel or consonant  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        char ch = s.next().charAt(0);
        
        if ("AEIOUaeiou".indexOf(ch) != -1) {
            System.out.println("Vowel");
        } else if (Character.isLetter(ch)) {
            System.out.println("Consonant");
        } else {
            System.out.println("Invalid Input");
        }
    }
}
```

**Input:**  
```
a
```
**Output:**  
```
Vowel
```

---

### 10. Find the smallest of three numbers  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        int c = s.nextInt();
        
        int min = Math.min(Math.min(a, b), c);
        System.out.println(min);
    }
}
```

**Input:**  
```
8 4 6
```
**Output:**  
```
4
```

### 11. Check if a number is prime or not using a simple loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        boolean isPrime = true;

        if (n <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i < n; i++) {
                if (n % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime) {
            System.out.println("Prime");
        } else {
            System.out.println("Not Prime");
        }
    }
}
```

**Input:**  
```
7
```
**Output:**  
```
Prime
```

---

### 12. Check if a number is perfect or not  
(A perfect number is a number equal to the sum of its proper divisors.)  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int sum = 0;

        for (int i = 1; i < n; i++) {
            if (n % i == 0) {
                sum += i;
            }
        }

        if (sum == n) {
            System.out.println("Perfect Number");
        } else {
            System.out.println("Not a Perfect Number");
        }
    }
}
```

**Input:**  
```
6
```
**Output:**  
```
Perfect Number
```

---

### 13. Check if a number is an Armstrong number  
(An Armstrong number is a number that is equal to the sum of its own digits raised to the power of the number of digits.)  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int temp = n, sum = 0, digits = 0;

        int num = n;
        while (num > 0) {
            digits++;
            num /= 10;
        }

        num = n;
        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits);
            num /= 10;
        }

        if (sum == n) {
            System.out.println("Armstrong Number");
        } else {
            System.out.println("Not an Armstrong Number");
        }
    }
}
```

**Input:**  
```
153
```
**Output:**  
```
Armstrong Number
```

---

### 14. Calculate the factorial of a number using recursion  
```java
import java.util.*;

public class Main {
    public static int factorial(int n) {
        if (n == 0 || n == 1) {
            return 1;
        }
        return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        System.out.println(factorial(n));
    }
}
```

**Input:**  
```
5
```
**Output:**  
```
120
```

---

### 15. Check whether a number is an automorphic number  
(An automorphic number is a number whose square ends with the number itself.)  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int square = n * n;
        
        String numStr = String.valueOf(n);
        String squareStr = String.valueOf(square);
        
        if (squareStr.endsWith(numStr)) {
            System.out.println("Automorphic Number");
        } else {
            System.out.println("Not an Automorphic Number");
        }
    }
}
```

**Input:**  
```
25
```
**Output:**  
```
Automorphic Number
```



### 17. Determine if a number is a perfect square  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int sqrt = (int) Math.sqrt(n);
        
        if (sqrt * sqrt == n) {
            System.out.println("Perfect Square");
        } else {
            System.out.println("Not a Perfect Square");
        }
    }
}
```

**Input:**  
```
16
```
**Output:**  
```
Perfect Square
```

---

### 18. Count the number of digits in a number  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int count = 0;

        while (n > 0) {
            count++;
            n /= 10;
        }

        System.out.println(count);
    }
}
```

**Input:**  
```
12345
```
**Output:**  
```
5
```

---

### 19. Check whether a string is a palindrome  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str = s.next();
        String rev = new StringBuilder(str).reverse().toString();
        
        if (str.equals(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }
    }
}
```

**Input:**  
```
madam
```
**Output:**  
```
Palindrome
```

---

### 20. Check if a string is an anagram of another string  
```java
import java.util.*;

public class Main {
    public static boolean areAnagrams(String str1, String str2) {
        char[] arr1 = str1.toCharArray();
        char[] arr2 = str2.toCharArray();
        Arrays.sort(arr1);
        Arrays.sort(arr2);
        return Arrays.equals(arr1, arr2);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str1 = s.next();
        String str2 = s.next();
        
        if (areAnagrams(str1, str2)) {
            System.out.println("Anagram");
        } else {
            System.out.println("Not an Anagram");
        }
    }
}
```

**Input:**  
```
listen silent
```
**Output:**  
```
Anagram
```


### 21. Check whether a number is a prime number within a range  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        for (int num = start; num <= end; num++) {
            boolean isPrime = true;
            if (num <= 1) {
                isPrime = false;
            } else {
                for (int i = 2; i < num; i++) {
                    if (num % i == 0) {
                        isPrime = false;
                        break;
                    }
                }
            }
            if (isPrime) {
                System.out.println(num);
            }
        }
    }
}
```

**Input:**  
```
10 20
```
**Output:**  
```
11
13
17
19
```

---

### 22. Find the largest number among n numbers using a nested if-else  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int max = s.nextInt();

        for (int i = 1; i < n; i++) {
            int num = s.nextInt();
            if (num > max) {
                max = num;
            }
        }

        System.out.println(max);
    }
}
```

**Input:**  
```
5
10 20 5 30 25
```
**Output:**  
```
30
```

---

### 23. Print all prime numbers in a range using nested loops  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        for (int num = start; num <= end; num++) {
            boolean isPrime = true;
            if (num <= 1) {
                isPrime = false;
            } else {
                for (int i = 2; i * i <= num; i++) {
                    if (num % i == 0) {
                        isPrime = false;
                        break;
                    }
                }
            }
            if (isPrime) {
                System.out.println(num);
            }
        }
    }
}
```

---

### 24. Find all the divisors of a number  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();

        for (int i = 1; i <= n; i++) {
            if (n % i == 0) {
                System.out.println(i);
            }
        }
    }
}
```

**Input:**  
```
12
```
**Output:**  
```
1
2
3
4
6
12
```

---

### 25. Find the GCD and LCM of two numbers  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        int gcd = 1;

        for (int i = 1; i <= a && i <= b; i++) {
            if (a % i == 0 && b % i == 0) {
                gcd = i;
            }
        }

        int lcm = (a * b) / gcd;
        System.out.println("GCD: " + gcd);
        System.out.println("LCM: " + lcm);
    }
}
```

---

### 26. Check if a number is a perfect number within a range  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        for (int n = start; n <= end; n++) {
            int sum = 0;
            for (int i = 1; i < n; i++) {
                if (n % i == 0) {
                    sum += i;
                }
            }
            if (sum == n) {
                System.out.println(n);
            }
        }
    }
}
```

---

### 27. Check whether an integer is positive, negative, or zero  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();

        if (num > 0) {
            System.out.println("Positive");
        } else if (num < 0) {
            System.out.println("Negative");
        } else {
            System.out.println("Zero");
        }
    }
}
```

---

### 28. Determine the type of a triangle based on its angles  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();
        int c = s.nextInt();

        if (a + b + c != 180) {
            System.out.println("Not a Triangle");
        } else if (a == 90 || b == 90 || c == 90) {
            System.out.println("Right-angled Triangle");
        } else if (a > 90 || b > 90 || c > 90) {
            System.out.println("Obtuse Triangle");
        } else {
            System.out.println("Acute Triangle");
        }
    }
}
```

---

### 29. Find whether a number is a Fibonacci number within a range  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();
        int a = 0, b = 1, c = 0;

        while (c <= end) {
            if (c >= start) {
                System.out.println(c);
            }
            c = a + b;
            a = b;
            b = c;
        }
    }
}
```

---

### 30. Print all leap years within a given range  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        for (int year = start; year <= end; year++) {
            if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
                System.out.println(year);
            }
        }
    }
}
```
You're right! I'll make sure to include input and output examples for all programs. Here’s the corrected set:  

---

### 31. Check whether a string is a valid palindrome  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str = s.next();
        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev += str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }
    }
}
```

**Input:**  
```
madam
```
**Output:**  
```
Palindrome
```

---

### 32. Check for a specific pattern in a string using if-else  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str = s.next();

        if (str.startsWith("AI")) {
            System.out.println("Starts with AI");
        } else if (str.endsWith("DS")) {
            System.out.println("Ends with DS");
        } else {
            System.out.println("No specific pattern found");
        }
    }
}
```

**Input:**  
```
AIProject
```
**Output:**  
```
Starts with AI
```

---

### 33. Check if a given day is a weekend or weekday  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String day = s.next().toLowerCase();

        if (day.equals("saturday") || day.equals("sunday")) {
            System.out.println("Weekend");
        } else {
            System.out.println("Weekday");
        }
    }
}
```

**Input:**  
```
Monday
```
**Output:**  
```
Weekday
```

---

### 34. Check if a number is divisible by 7 or 11  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();

        if (num % 7 == 0 && num % 11 == 0) {
            System.out.println("Divisible by both 7 and 11");
        } else if (num % 7 == 0) {
            System.out.println("Divisible by 7");
        } else if (num % 11 == 0) {
            System.out.println("Divisible by 11");
        } else {
            System.out.println("Not divisible by 7 or 11");
        }
    }
}
```

**Input:**  
```
77
```
**Output:**  
```
Divisible by both 7 and 11
```

---

### 35. Print prime numbers within a range using nested conditions  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        for (int num = start; num <= end; num++) {
            boolean isPrime = true;

            if (num <= 1) {
                isPrime = false;
            } else {
                for (int i = 2; i * i <= num; i++) {
                    if (num % i == 0) {
                        isPrime = false;
                        break;
                    }
                }
            }

            if (isPrime) {
                System.out.println(num);
            }
        }
    }
}
```

**Input:**  
```
10 20
```
**Output:**  
```
11
13
17
19
```

---

### 36. Identify if an alphabet character is uppercase, lowercase, or non-alphabet  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        char ch = s.next().charAt(0);

        if (ch >= 'A' && ch <= 'Z') {
            System.out.println("Uppercase Letter");
        } else if (ch >= 'a' && ch <= 'z') {
            System.out.println("Lowercase Letter");
        } else {
            System.out.println("Not an Alphabet");
        }
    }
}
```

**Input:**  
```
G
```
**Output:**  
```
Uppercase Letter
```



### **37. Check if a given number is a valid credit card number (Simpler Approach)**
Instead of implementing the full Luhn Algorithm, we can check if the card number has a common valid length (13, 15, or 16 digits). This is a basic validation.  

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String cardNumber = s.next();

        if (cardNumber.length() == 13 || cardNumber.length() == 15 || cardNumber.length() == 16) {
            System.out.println("Valid Card Length");
        } else {
            System.out.println("Invalid Card Length");
        }
    }
}
```

**Input:**  
```
4532015112830366
```
**Output:**  
```
Valid Card Length
```

---

### **38. Check if a given date is valid (Simpler Approach)**  
Instead of checking for leap years and specific months, we use **Java's built-in `LocalDate` class** which automatically handles invalid dates.  

```java
import java.util.*;
import java.time.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int day = s.nextInt();
        int month = s.nextInt();
        int year = s.nextInt();

        try {
            LocalDate date = LocalDate.of(year, month, day);
            System.out.println("Valid Date");
        } catch (Exception e) {
            System.out.println("Invalid Date");
        }
    }
}
```

**Input:**  
```
30 2 2024
```
**Output:**  
```
Invalid Date
```

---

### **39. Find the day of the week for a given date (Simpler Approach)**  
Instead of using `Calendar`, we use **Java's built-in `LocalDate` and `getDayOfWeek()`** for a much simpler solution.  

```java
import java.util.*;
import java.time.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int day = s.nextInt();
        int month = s.nextInt();
        int year = s.nextInt();

        LocalDate date = LocalDate.of(year, month, day);
        System.out.println(date.getDayOfWeek());
    }
}
```

**Input:**  
```
10 2 2025
```
**Output:**  
```
MONDAY
```

---


### 40. Print multiplication tables for a given number using nested loops  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();

        for (int i = 1; i <= 10; i++) {
            System.out.println(num + " x " + i + " = " + (num * i));
        }
    }
}
```

**Input:**  
```
5
```
**Output:**  
```
5 x 1 = 5
...
...
...
5 x 10 = 50
```


### **41. Implement a simple calculator using switch case**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = s.nextInt();

        System.out.print("Enter operator (+, -, *, /): ");
        char op = s.next().charAt(0);

        System.out.print("Enter second number: ");
        int b = s.nextInt();

        switch (op) {
            case '+': System.out.println("Result: " + (a + b)); break;
            case '-': System.out.println("Result: " + (a - b)); break;
            case '*': System.out.println("Result: " + (a * b)); break;
            case '/': 
                if (b != 0) System.out.println("Result: " + (a / b));
                else{
                     System.out.println("Cannot divide by zero");
                     }
                break;
            default: System.out.println("Invalid operator");
        }
    }
}
```

---

### **42. Convert a number to its word equivalent (1 to 10) using switch**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        
        System.out.print("Enter a number (1-10): ");
        int num = s.nextInt();
        
        switch (num) {
            case 1: System.out.println("One"); break;
            case 2: System.out.println("Two"); break;
            case 3: System.out.println("Three"); break;
            case 4: System.out.println("Four"); break;
            case 5: System.out.println("Five"); break;
            case 6: System.out.println("Six"); break;
            case 7: System.out.println("Seven"); break;
            case 8: System.out.println("Eight"); break;
            case 9: System.out.println("Nine"); break;
            case 10: System.out.println("Ten"); break;
            default: System.out.println("Invalid number");
        }
    }
}
```

---

### **43. Find the day of the week using switch statement**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number (1-7): ");
        int day = s.nextInt();

        switch (day) {
            case 1: System.out.println("Sunday"); break;
            case 2: System.out.println("Monday"); break;
            case 3: System.out.println("Tuesday"); break;
            case 4: System.out.println("Wednesday"); break;
            case 5: System.out.println("Thursday"); break;
            case 6: System.out.println("Friday"); break;
            case 7: System.out.println("Saturday"); break;
            default: System.out.println("Invalid input");
        }
    }
}
```

---

### **44. Convert a number to its Roman numeral equivalent using switch**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number (1-10): ");
        int num = s.nextInt();

        switch (num) {
            case 1: System.out.println("I"); break;
            case 2: System.out.println("II"); break;
            case 3: System.out.println("III"); break;
            case 4: System.out.println("IV"); break;
            case 5: System.out.println("V"); break;
            case 6: System.out.println("VI"); break;
            case 7: System.out.println("VII"); break;
            case 8: System.out.println("VIII"); break;
            case 9: System.out.println("IX"); break;
            case 10: System.out.println("X"); break;
            default: System.out.println("Invalid number");
        }
    }
}
```

---

### **45. Implement a basic menu-driven program using switch-case**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.println("Menu:");
        System.out.println("1. Say Hello");
        System.out.println("2. Say Goodbye");
        System.out.println("3. Exit");
        
        System.out.print("Enter your choice: ");
        int choice = s.nextInt();

        switch (choice) {
            case 1: System.out.println("Hello!"); break;
            case 2: System.out.println("Goodbye!"); break;
            case 3: System.out.println("Exiting..."); break;
            default: System.out.println("Invalid choice");
        }
    }
}
```

---

### **46. Print all numbers from 1 to n in reverse using switch**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int n = s.nextInt();

        switch (1) {
            case 1:
                for (int i = n; i >= 1; i--) {
                    System.out.print(i + " ");
                }
        }
    }
}
```

---

### **47. Grade student marks using a switch-case statement**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter marks (0-100): ");
        int marks = s.nextInt();
        
        switch (marks / 10) {
            
            case 9: System.out.println("Grade: A"); break;
            case 8: System.out.println("Grade: B"); break;
            case 7: System.out.println("Grade: C"); break;
            case 6: System.out.println("Grade: D"); break;
            case 4: System.out.println("Grade: E"); break;
            default: System.out.println("Grade: F");
        }
    }
}
```



---

### **49. Convert temperature from Celsius to Fahrenheit or vice versa using switch**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.println("1. Celsius to Fahrenheit");
        System.out.println("2. Fahrenheit to Celsius");
        
        System.out.print("Enter choice: ");
        int choice = s.nextInt();

        System.out.print("Enter temperature: ");
        float temp = s.nextFloat();

        switch (choice) {
            case 1: System.out.println("Fahrenheit: " + ((temp * 9 / 5) + 32)); break;
            case 2: System.out.println("Celsius: " + ((temp - 32) * 5 / 9)); break;
            default: System.out.println("Invalid choice");
        }
    }
}
```

---

### **50. Find the number of days in a month using switch-case**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter month number (1-12): ");
        int month = s.nextInt();

        switch (month) {
            case 1: case 3: case 5: case 7: case 8: case 10: case 12:
                System.out.println("31 days"); break;
            case 4: case 6: case 9: case 11:
                System.out.println("30 days"); break;
            case 2:
                System.out.println("28 or 29 days"); break;
            default:
                System.out.println("Invalid month");
        }
    }
}
```

### **51. Implement a simple banking system with switch-case**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int balance = 1000;

        System.out.println("1. Check Balance");
        System.out.println("2. Deposit");
        System.out.println("3. Withdraw");
        System.out.print("Enter your choice: ");
        int choice = s.nextInt();

        switch (choice) {
            case 1: System.out.println("Balance: $" + balance); break;
            case 2: 
                System.out.print("Enter amount to deposit: ");
                int deposit = s.nextInt();
                balance += deposit;
                System.out.println("New Balance: $" + balance);
                break;
            case 3:
                System.out.print("Enter amount to withdraw: ");
                int withdraw = s.nextInt();
                if (withdraw <= balance) {
                    balance -= withdraw;
                    System.out.println("New Balance: $" + balance);
                } else {
                    System.out.println("Insufficient balance");
                }
                break;
            default: System.out.println("Invalid choice");
        }
    }
}
```

---

### **52. Determine the month name based on its number using switch-case**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        
        System.out.print("Enter month number (1-12): ");
        int month = s.nextInt();
        
        switch (month) {
            case 1: System.out.println("January"); break;
            case 2: System.out.println("February"); break;
            case 3: System.out.println("March"); break;
            case 4: System.out.println("April"); break;
            case 5: System.out.println("May"); break;
            case 6: System.out.println("June"); break;
            case 7: System.out.println("July"); break;
            case 8: System.out.println("August"); break;
            case 9: System.out.println("September"); break;
            case 10: System.out.println("October"); break;
            case 11: System.out.println("November"); break;
            case 12: System.out.println("December"); break;
            default: System.out.println("Invalid month");
        }
    }
}
```

---

### **53. Calculate the area of different shapes using switch-case**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.println("1. Circle");
        System.out.println("2. Rectangle");
        System.out.println("3. Triangle");
        System.out.print("Enter your choice: ");
        int choice = s.nextInt();

        switch (choice) {
            case 1:
                System.out.print("Enter radius: ");
                float r = s.nextFloat();
                System.out.println("Area: " + (3.14 * r * r));
                break;
            case 2:
                System.out.print("Enter length: ");
                float l = s.nextFloat();
                System.out.print("Enter width: ");
                float w = s.nextFloat();
                System.out.println("Area: " + (l * w));
                break;
            case 3:
                System.out.print("Enter base: ");
                float b = s.nextFloat();
                System.out.print("Enter height: ");
                float h = s.nextFloat();
                System.out.println("Area: " + (0.5 * b * h));
                break;
            default: System.out.println("Invalid choice");
        }
    }
}
```


### **55. Determine if a given character is a vowel or consonant using switch-case**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        
        System.out.print("Enter a character: ");
        char ch = s.next().toLowerCase().charAt(0);
        
        switch (ch) {
            case 'a': case 'e': case 'i': case 'o': case 'u':
                System.out.println("Vowel");
                break;
            default:
                if (Character.isLetter(ch)) System.out.println("Consonant");
                else System.out.println("Not a letter");
        }
    }
}
```

---

### **56. Implement a simple menu system for shopping**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.println("1. Buy Apple - $2");
        System.out.println("2. Buy Banana - $1");
        System.out.println("3. Buy Orange - $3");
        System.out.print("Enter your choice: ");
        int choice = s.nextInt();

        switch (choice) {
            case 1: System.out.println("You bought an Apple"); break;
            case 2: System.out.println("You bought a Banana"); break;
            case 3: System.out.println("You bought an Orange"); break;
            default: System.out.println("Invalid choice");
        }
    }
}
```

---

### **57. Convert a time duration in minutes to hours and minutes**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter time in minutes: ");
        int minutes = s.nextInt();

        int hours = minutes / 60;
        int remainingMinutes = minutes % 60;

        System.out.println("Time: " + hours + " hours " + remainingMinutes + " minutes");
    }
}
```



### **59. Implement a traffic light system using switch**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter traffic light color (Red, Yellow, Green): ");
        String color = s.next().toLowerCase();

        switch (color) {
            case "red": System.out.println("Stop!"); break;
            case "yellow": System.out.println("Get Ready!"); break;
            case "green": System.out.println("Go!"); break;
            default: System.out.println("Invalid color");
        }
    }
}
```

---

### **60. Solve a quadratic equation using switch-case for the discriminant**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter coefficient a: ");
        double a = s.nextDouble();
        System.out.print("Enter coefficient b: ");
        double b = s.nextDouble();
        System.out.print("Enter coefficient c: ");
        double c = s.nextDouble();

        double d = (b * b) - (4 * a * c);

        switch (d > 0 ? 1 : (d == 0 ? 0 : -1)) {
            case 1:
                double root1 = (-b + Math.sqrt(d)) / (2 * a);
                double root2 = (-b - Math.sqrt(d)) / (2 * a);
                System.out.println("Two Real Roots: " + root1 + " and " + root2);
                break;
            case 0:
                double root = -b / (2 * a);
                System.out.println("One Real Root: " + root);
                break;
            case -1:
                System.out.println("No Real Roots");
                break;
        }
    }
}


## **61. Print numbers from 1 to 10 using for loop**
### **Code**
```java
public class Main {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            System.out.print(i + " ");
        }
    }
}
```
### **Output**
```
1 2 3 4 5 6 7 8 9 10
```

---

## **62. Print the multiplication table of a number using for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = s.nextInt();

        for (int i = 1; i <= 10; i++) {
            System.out.println(num + " x " + i + " = " + (num * i));
        }
    }
}
```
### **Input**
```
Enter a number: 5
```
### **Output**
```
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

---

## **63. Calculate the factorial of a number using a for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = s.nextInt();
        int fact = 1;

        for (int i = 1; i <= num; i++) {
            fact *= i;
        }

        System.out.println("Factorial: " + fact);
    }
}
```
### **Input**
```
Enter a number: 5
```
### **Output**
```
Factorial: 120
```

---

## **64. Print Fibonacci series up to n terms using for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter number of terms: ");
        int n = s.nextInt();

        int a = 0, b = 1;
        System.out.print(a + " " + b + " ");

        for (int i = 3; i <= n; i++) {
            int next = a + b;
            System.out.print(next + " ");
            a = b;
            b = next;
        }
    }
}
```
### **Input**
```
Enter number of terms: 6
```
### **Output**
```
0 1 1 2 3 5
```

---

## **65. Sum of digits of a number using a for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = s.nextInt();
        int sum = 0;

        for (; num > 0; num /= 10) {
            sum += num % 10;
        }

        System.out.println("Sum of digits: " + sum);
    }
}
```
### **Input**
```
Enter a number: 123
```
### **Output**
```
Sum of digits: 6
```

---

## **66. Print prime numbers up to a given number using for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int n = s.nextInt();

        for (int i = 2; i <= n; i++) {
            boolean isPrime = true;
            for (int j = 2; j * j <= i; j++) {
                if (i % j == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime) System.out.print(i + " ");
        }
    }
}
```
### **Input**
```
Enter a number: 20
```
### **Output**
```
2 3 5 7 11 13 17 19
```

---

## **67. Reverse a number using for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = s.nextInt();
        int rev = 0;

        while(num>0) {
           num=num/10;
            rev = rev * 10 + num % 10;
        }

        System.out.println("Reversed Number: " + rev);
    }
}
```
### **Input**
```
Enter a number: 1234
```
### **Output**
```
Reversed Number: 4321
```

---

## **68. Check whether a number is prime or not using a for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = s.nextInt();
        boolean isPrime = true;

        for (int i = 2; i * i <= num; i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }

        if (isPrime && num > 1) {
       System.out.println("Prime");
}
        else{
 System.out.println("Not Prime");
}
    }
}
```
### **Input**
```
Enter a number: 17
```
### **Output**
```
Prime
```

---

## **69. Calculate the sum of even numbers from 1 to n using a for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter n: ");
        int n = s.nextInt();
        int sum = 0;

        for (int i = 2; i <= n; i += 2) {
            sum += i;
        }

        System.out.println("Sum of even numbers: " + sum);
    }
}
```
### **Input**
```
Enter n: 10
```
### **Output**
```
Sum of even numbers: 30
```

---

## **70. Calculate the sum of odd numbers from 1 to n using a for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter n: ");
        int n = s.nextInt();
        int sum = 0;

        for (int i = 1; i <= n; i += 2) {
            sum += i;
        }

        System.out.println("Sum of odd numbers: " + sum);
    }
}
```
### **Input**
```
Enter n: 10
```
### **Output**
```
Sum of odd numbers: 25
```



## **71. Print a pyramid pattern using for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter number of rows: ");
        int n = s.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n - i; j++) System.out.print(" ");
            for (int j = 1; j <= 2 * i - 1; j++) System.out.print("*");
            System.out.println();
        }
    }
}
```
### **Input**
```
Enter number of rows: 5
```
### **Output**
```
    *  
   ***  
  *****  
 *******  
*********
```

---

## **72. Print a reverse triangle pattern using for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter number of rows: ");
        int n = s.nextInt();

        for (int i = n; i >= 1; i--) {
            for (int j = 1; j <= n - i; j++){
          System.out.print(" ");
}
            for (int j = 1; j <= 2 * i - 1; j++){
           System.out.print("*");
}
            System.out.println();
        }
    }
}
```
### **Input**
```
Enter number of rows: 5
```
### **Output**
```
*********
 *******  
  *****  
   ***  
    *  
```

---

## **73. Find the largest number in an array using a for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter the number of elements: ");
        int n = s.nextInt();
        int arr[] = new int[n];

        System.out.println("Enter the elements: ");
        for (int i = 0; i < n; i++) {
            arr[i] = s.nextInt();
        }

        int max = arr[0];
        for (int i = 1; i < n; i++) {
            if (arr[i] > max) {
                max = arr[i];
            }
        }

        System.out.println("Largest number: " + max);
    }
}
```
### **Input**
```
Enter the number of elements: 5
Enter the elements:
10 25 36 5 12
```
### **Output**
```
Largest number: 36
```

---

## **74. Print a series of squares (1, 4, 9, ...) using for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter n: ");
        int n = s.nextInt();

        for (int i = 1; i <= n; i++) {
            System.out.print((i * i) + " ");
        }
    }
}
```
### **Input**
```
Enter n: 5
```
### **Output**
```
1 4 9 16 25
```

---

## **75. Count the number of even numbers in a range**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter start number: ");
        int start = s.nextInt();
        System.out.print("Enter end number: ");
        int end = s.nextInt();

        int count = 0;
        for (int i = start; i <= end; i++) {
            if (i % 2 == 0) {
                count++;
            }
        }

        System.out.println("Count of even numbers: " + count);
    }
}
```
### **Input**
```
Enter start number: 1
Enter end number: 10
```
### **Output**
```
Count of even numbers: 5
```

---

## **76. Print all prime numbers between two numbers**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter start number: ");
        int start = s.nextInt();
        System.out.print("Enter end number: ");
        int end = s.nextInt();

        for (int i = start; i <= end; i++) {
            boolean isPrime = true;
            if (i < 2) continue;
            for (int j = 2; j * j <= i; j++) {
                if (i % j == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime) System.out.print(i + " ");
        }
    }
}
```
### **Input**
```
Enter start number: 10
Enter end number: 30
```
### **Output**
```
11 13 17 19 23 29
```

---

## **77. Find the sum of all elements in an array using a for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter the number of elements: ");
        int n = s.nextInt();
        int arr[] = new int[n];

        System.out.println("Enter the elements: ");
        for (int i = 0; i < n; i++) {
            arr[i] = s.nextInt();
        }

        int sum = 0;
        for (int i = 0; i < n; i++) {
            sum += arr[i];
        }

        System.out.println("Sum of elements: " + sum);
    }
}
```
### **Input**
```
Enter the number of elements: 5
Enter the elements:
10 20 30 40 50
```
### **Output**
```
Sum of elements: 150
```

---

## **78. Calculate the average of an array using a for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter the number of elements: ");
        int n = s.nextInt();
        int arr[] = new int[n];

        System.out.println("Enter the elements: ");
        for (int i = 0; i < n; i++) {
            arr[i] = s.nextInt();
        }

        int sum = 0;
        for (int i = 0; i < n; i++) {
            sum += arr[i];
        }

        double average = (double) sum / n;
        System.out.println("Average: " + average);
    }
}
```
### **Input**
```
Enter the number of elements: 5
Enter the elements:
10 20 30 40 50
```
### **Output**
```
Average: 30.0
```

## **79. Print a number pattern using for loop**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter number of rows: ");
        int n = s.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```
### **Input**
```
Enter number of rows: 5
```
### **Output**
```
1  
1 2  
1 2 3  
1 2 3 4  
1 2 3 4 5
```

---

## **80. Print Pascal’s Triangle using nested for loops**
### **Code**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter number of rows: ");
        int n = s.nextInt();
        for (int i = 0; i < n; i++) {
            for (int j = 0; j <= n - i; j++) {
                System.out.print(" ");
            }
            int num = 1;
            for (int j = 0; j <= i; j++) {
                System.out.print(num + " ");
                num = num * (i - j) / (j + 1);
            }
            System.out.println();
        }
    }
}
```
### **Input**
```
Enter number of rows: 5
```
### **Output**
```
     1  
    1 1  
   1 2 1  
  1 3 3 1  
 1 4 6 4 1  
```




## **81-90: Java Programs Using While Loop**
---

### **81. Print numbers from 1 to 10 using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 10) {
            System.out.print(i + " ");
            i++;
        }
    }
}
```
**Output:**  
```
1 2 3 4 5 6 7 8 9 10
```

---

### **82. Print all even numbers up to n using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int i = 2;
        
        while (i <= n) {
            System.out.print(i + " ");
            i += 2;
        }
    }
}
```
**Input:**  
```
10
```
**Output:**  
```
2 4 6 8 10
```

---

### **83. Calculate the factorial of a number using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int fact = 1, i = 1;

        while (i <= n) {
            fact *= i;
            i++;
        }
        System.out.println(fact);
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
120
```

---

### **84. Reverse a number using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int rev = 0;
        
        while (num > 0) {
            rev = rev * 10 + num % 10;
            num /= 10;
        }
        System.out.println(rev);
    }
}
```
**Input:**  
```
1234
```
**Output:**  
```
4321
```

---

### **85. Print Fibonacci series up to n terms using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int a = 0, b = 1, count = 0;
        
        while (count < n) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
            count++;
        }
    }
}
```
**Input:**  
```
7
```
**Output:**  
```
0 1 1 2 3 5 8
```

---

### **86. Sum of digits of a number using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int sum = 0;

        while (num > 0) {
            sum += num % 10;
            num /= 10;
        }
        System.out.println(sum);
    }
}
```
**Input:**  
```
123
```
**Output:**  
```
6
```

---

### **87. Print all odd numbers up to n using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int i = 1;

        while (i <= n) {
            System.out.print(i + " ");
            i += 2;
        }
    }
}
```
**Input:**  
```
10
```
**Output:**  
```
1 3 5 7 9
```

---

### **88. Find the sum of natural numbers using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int sum = 0, i = 1;

        while (i <= n) {
            sum += i;
            i++;
        }
        System.out.println(sum);
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
15
```

---

### **89. Count the number of digits in a number using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int count = 0;

        while (num > 0) {
            count++;
            num /= 10;
        }
        System.out.println(count);
    }
}
```
**Input:**  
```
7896
```
**Output:**  
```
4
```

---

### **90. Calculate the product of digits of a number using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int product = 1;

        while (num > 0) {
            product *= num % 10;
            num /= 10;
        }
        System.out.println(product);
    }
}
```
**Input:**  
```
234
```
**Output:**  
```
24
```


### **91. Find the largest prime number in a given range**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();
        int largestPrime = -1;

        while (end >= start) {
            int i = 2, flag = 1;
            if (end < 2) break;
            while (i * i <= end) {
                if (end % i == 0) {
                    flag = 0;
                    break;
                }
                i++;
            }
            if (flag == 1) {
                largestPrime = end;
                break;
            }
            end--;
        }
        System.out.println(largestPrime);
    }
}
```
**Input:**  
```
10 50
```
**Output:**  
```
47
```

---

### **92. Print all prime numbers up to n using a while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int num = 2;

        while (num <= n) {
            int i = 2, flag = 1;
            while (i * i <= num) {
                if (num % i == 0) {
                    flag = 0;
                    break;
                }
                i++;
            }
            if (flag == 1) System.out.print(num + " ");
            num++;
        }
    }
}
```
**Input:**  
```
20
```
**Output:**  
```
2 3 5 7 11 13 17 19
```

---

### **93. Find the greatest common divisor (GCD) using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();

        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        System.out.println(a);
    }
}
```
**Input:**  
```
48 18
```
**Output:**  
```
6
```

---

### **94. Implement a simple ATM menu using a while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int balance = 1000;

        while (true) {
            int choice = s.nextInt();
            if (choice == 1) System.out.println(balance);
            else if (choice == 2) {
                int amount = s.nextInt();
                if (amount <= balance) balance -= amount;
            } else if (choice == 3) {
                int amount = s.nextInt();
                balance += amount;
            } else if (choice == 4) break;
        }
    }
}
```
**Input:**  
```
1
```
**Output:**  
```
1000
```

---

### **95. Reverse a string using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str = s.next();
        String rev = "";
        int i = str.length() - 1;

        while (i >= 0) {
            rev += str.charAt(i);
            i--;
        }
        System.out.println(rev);
    }
}
```
**Input:**  
```
hello
```
**Output:**  
```
olleh
```

---

### **96. Sum all odd numbers in a range using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();
        int sum = 0;

        while (start <= end) {
            if (start % 2 != 0) sum += start;
            start++;
        }
        System.out.println(sum);
    }
}
```
**Input:**  
```
1 10
```
**Output:**  
```
25
```

---

### **97. Check if a number is prime using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int i = 2, flag = 1;

        while (i * i <= num) {
            if (num % i == 0) {
                flag = 0;
                break;
            }
            i++;
        }
        System.out.println(flag == 1 && num > 1 ? "Prime" : "Not Prime");
    }
}
```
**Input:**  
```
17
```
**Output:**  
```
Prime
```

---

### **98. Find the factorial of a number using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int fact = 1;

        while (num > 1) {
            fact *= num;
            num--;
        }
        System.out.println(fact);
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
120
```

---

### **99. Print even numbers from a range using while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        while (start <= end) {
            if (start % 2 == 0) System.out.print(start + " ");
            start++;
        }
    }
}
```
**Input:**  
```
1 10
```
**Output:**  
```
2 4 6 8 10
```

---

### **100. Find the sum of even and odd digits of a number**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int evenSum = 0, oddSum = 0;

        while (num > 0) {
            int digit = num % 10;
            if (digit % 2 == 0) evenSum += digit;
            else oddSum += digit;
            num /= 10;
        }
        System.out.println(evenSum + " " + oddSum);
    }
}
```
**Input:**  
```
1234
```
**Output:**  
```
6 4
```


### **101. Print numbers from 1 to 10 using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        int i = 1;
        do {
            System.out.print(i + " ");
            i++;
        } while (i <= 10);
    }
}
```
**Output:**  
```
1 2 3 4 5 6 7 8 9 10
```

---

### **102. Sum of all even numbers using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();
        int sum = 0;

        do {
            if (start % 2 == 0) sum += start;
            start++;
        } while (start <= end);

        System.out.println(sum);
    }
}
```
**Input:**  
```
1 10
```
**Output:**  
```
30
```

---

### **103. Print all odd numbers in a range using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        do {
            if (start % 2 != 0) System.out.print(start + " ");
            start++;
        } while (start <= end);
    }
}
```
**Input:**  
```
1 10
```
**Output:**  
```
1 3 5 7 9
```

---

### **104. Calculate the factorial of a number using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int fact = 1;

        do {
            fact *= num;
            num--;
        } while (num > 1);

        System.out.println(fact);
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
120
```

---

### **105. Reverse a number using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int rev = 0;

        do {
            rev = rev * 10 + num % 10;
            num /= 10;
        } while (num > 0);

        System.out.println(rev);
    }
}
```
**Input:**  
```
1234
```
**Output:**  
```
4321
```

---

### **106. Count the number of digits in a number using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int count = 0;

        do {
            count++;
            num /= 10;
        } while (num > 0);

        System.out.println(count);
    }
}
```
**Input:**  
```
1234
```
**Output:**  
```
4
```

---

### **107. Check if a number is prime using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num = s.nextInt();
        int i = 2, flag = 1;

        do {
            if (num % i == 0) {
                flag = 0;
                break;
            }
            i++;
        } while (i * i <= num);

        if (flag == 1 && num > 1) System.out.println("Prime");
        else System.out.println("Not Prime");
    }
}
```
**Input:**  
```
17
```
**Output:**  
```
Prime
```

---

### **108. Find the GCD of two numbers using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        int b = s.nextInt();

        do {
            int temp = b;
            b = a % b;
            a = temp;
        } while (b != 0);

        System.out.println(a);
    }
}
```
**Input:**  
```
48 18
```
**Output:**  
```
6
```

---

### **109. Print Fibonacci series up to n terms using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int a = 0, b = 1, i = 0;

        do {
            System.out.print(a + " ");
            int temp = a + b;
            a = b;
            b = temp;
            i++;
        } while (i < n);
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
0 1 1 2 3
```

---

### **110. Check if a string is a palindrome using do-while loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str = s.next();
        int i = 0, j = str.length() - 1, flag = 1;

        do {
            if (str.charAt(i) != str.charAt(j)) {
                flag = 0;
                break;
            }
            i++;
            j--;
        } while (i < j);

        if (flag == 1) System.out.println("Palindrome");
        else System.out.println("Not Palindrome");
    }
}
```
**Input:**  
```
madam
```
**Output:**  
```
Palindrome
```



### 111. Print a Pattern of Stars Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int i = 1;
        
        do {
            int j = 1;
            do {
                System.out.print("* ");
                j++;
            } while (j <= i);
            System.out.println();
            i++;
        } while (i <= n);
    }
}
```

---

### 112. Sum All Digits of a Number Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int sum = 0;
        
        do {
            sum += n % 10;
            n /= 10;
        } while (n > 0);
        
        System.out.println(sum);
    }
}
```

---

### 113. Reverse a String Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str = s.next();
        String rev = "";
        int i = str.length() - 1;
        
        do {
            rev += str.charAt(i);
            i--;
        } while (i >= 0);
        
        System.out.println(rev);
    }
}
```

---

### 114. Find the Largest Prime Number in a Given Range Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();
        int largestPrime = -1;
        
        do {
            if (isPrime(end)) {
                largestPrime = end;
                break;
            }
            end--;
        } while (end >= start);
        
        System.out.println(largestPrime);
    }
    
    public static boolean isPrime(int n) {
        if (n < 2) return false;
        int i = 2;
        do {
            if (n % i == 0) return false;
            i++;
        } while (i * i <= n);
        return true;
    }
}
```

---

### 115. Print All Numbers Divisible by 5 Within a Range Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();
        
        do {
            if (start % 5 == 0) {
                System.out.println(start);
            }
            start++;
        } while (start <= end);
    }
}
```

---

### 116. Calculate the Sum of Squares of Numbers in a Range Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();
        int sum = 0;
        
        do {
            sum += start * start;
            start++;
        } while (start <= end);
        
        System.out.println(sum);
    }
}
```

---

### 117. Print the Fibonacci Sequence Up to a Given Limit Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int limit = s.nextInt();
        int a = 0, b = 1;
        
        do {
            System.out.println(a);
            int temp = a + b;
            a = b;
            b = temp;
        } while (a <= limit);
    }
}
```

---

### 118. Check If a Number Is a Perfect Number Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int sum = 0, i = 1;
        
        do {
            if (n % i == 0) {
                sum += i;
            }
            i++;
        } while (i <= n / 2);
        
        if (sum == n) {
            System.out.println("Perfect");
        } else {
            System.out.println("Not Perfect");
        }
    }
}
```

---

### 119. Find Armstrong Numbers in a Range Using `do-while` Loop  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();
        
        do {
            if (isArmstrong(start)) {
                System.out.println(start);
            }
            start++;
        } while (start <= end);
    }
    
    public static boolean isArmstrong(int num) {
        int temp = num, sum = 0, digits = String.valueOf(num).length();
        
        do {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        } while (temp > 0);
        
        return sum == num;
    }
}
```

### **121. Print a Multiplication Table Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        for (int i = 1; i <= 10; i++) {
            System.out.println(n + " x " + i + " = " + (n * i));
        }
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
5 x 1 = 5
5 x 2 = 10
...
5 x 10 = 50
```
---

### **122. Print an Inverted Triangle Pattern Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        for (int i = n; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
4
```
**Output:**  
```
* * * * 
* * *  
* *  
*  
```
---

### **123. Print a Pyramid Pattern Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        for (int i = 1; i <= n; i++) {
            for (int j = i; j < n; j++) {
                System.out.print(" ");
            }
            for (int j = 1; j <= (2 * i - 1); j++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
4
```
**Output:**  
```
   *  
  ***  
 *****  
*******
```
---

### **124. Print a Diamond Shape Pattern Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = i; j < n; j++) System.out.print(" ");
            for (int j = 1; j <= (2 * i - 1); j++) System.out.print("*");
            System.out.println();
        }
        for (int i = n - 1; i >= 1; i--) {
            for (int j = n; j > i; j--) System.out.print(" ");
            for (int j = 1; j <= (2 * i - 1); j++) System.out.print("*");
            System.out.println();
        }
    }
}
```
**Input:**  
```
3
```
**Output:**  
```
  *  
 ***  
*****  
 ***  
  *  
```
---

### **125. Print a Hollow Square Pattern Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                if (i == 1 || i == n || j == 1 || j == n)
                    System.out.print("* ");
                else
                    System.out.print("  ");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
* * * * *  
*       *  
*       *  
*       *  
* * * * *  
```
---

### **126. Print a Number Triangle Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
1  
1 2  
1 2 3  
1 2 3 4  
1 2 3 4 5  
```
---

### **127. Check for Prime Numbers Within a Range Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        for (int i = start; i <= end; i++) {
            boolean isPrime = true;
            for (int j = 2; j * j <= i; j++) {
                if (i % j == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime && i > 1) System.out.println(i);
        }
    }
}
```
**Input:**  
```
10 20
```
**Output:**  
```
11  
13  
17  
19  
```
---

### **128. Generate Pascal's Triangle Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();

        for (int i = 0; i < n; i++) {
            int num = 1;
            for (int j = 0; j <= i; j++) {
                System.out.print(num + " ");
                num = num * (i - j) / (j + 1);
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
1  
1 1  
1 2 1  
1 3 3 1  
1 4 6 4 1  
```

---

### **129. Print a Number Pattern with Asterisks Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j + " ");
            }
            System.out.print("* ");
            System.out.println();
        }
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
1 *  
1 2 *  
1 2 3 *  
1 2 3 4 *  
1 2 3 4 5 *  
```
---

### **130. Print All Possible Combinations of Two Arrays Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        
        int n = s.nextInt();
        int[] arr1 = new int[n];
        for (int i = 0; i < n; i++) arr1[i] = s.nextInt();
        
        int m = s.nextInt();
        int[] arr2 = new int[m];
        for (int i = 0; i < m; i++) arr2[i] = s.nextInt();
        
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                System.out.println(arr1[i] + ", " + arr2[j]);
            }
        }
    }
}
```
**Input:**  
```
3  
1 2 3  
2  
4 5  
```
**Output:**  
```
1, 4  
1, 5  
2, 4  
2, 5  
3, 4  
3, 5  
```
---

### **131. Create a Matrix and Perform Transpose Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int rows = s.nextInt();
        int cols = s.nextInt();
        int[][] matrix = new int[rows][cols];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = s.nextInt();
            }
        }

        System.out.println("Transpose:");
        for (int j = 0; j < cols; j++) {
            for (int i = 0; i < rows; i++) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
2 3  
1 2 3  
4 5 6  
```
**Output:**  
```
Transpose:  
1 4  
2 5  
3 6  
```
---

### **132. Count the Number of Vowels and Consonants in a String Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str = s.nextLine().toLowerCase();
        
        int vowels = 0, consonants = 0;
        String vowelSet = "aeiou";
        
        for (char ch : str.toCharArray()) {
            if (Character.isLetter(ch)) {
                if (vowelSet.indexOf(ch) != -1) vowels++;
                else consonants++;
            }
        }
        
        System.out.println("Vowels: " + vowels);
        System.out.println("Consonants: " + consonants);
    }
}
```
**Input:**  
```
hello world
```
**Output:**  
```
Vowels: 3  
Consonants: 7  
```
---

### **133. Create a Multiplication Matrix Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                System.out.print((i * j) + "\t");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
3
```
**Output:**  
```
1   2   3  
2   4   6  
3   6   9  
```
---

### **134. Print an Alphabet Pattern Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        
        for (int i = 0; i < n; i++) {
            for (int j = 0; j <= i; j++) {
                System.out.print((char) ('A' + j) + " ");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
4
```
**Output:**  
```
A  
A B  
A B C  
A B C D  
```

### **135. Find All Prime Numbers Between Two Numbers Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt();
        int end = s.nextInt();

        for (int i = start; i <= end; i++) {
            boolean isPrime = true;
            for (int j = 2; j * j <= i; j++) {
                if (i % j == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime && i > 1) System.out.println(i);
        }
    }
}
```
**Input:**  
```
10 20
```
**Output:**  
```
11  
13  
17  
19  
```
---

### **136. Create a 2D Array and Initialize It with User Input Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int rows = s.nextInt();
        int cols = s.nextInt();
        int[][] matrix = new int[rows][cols];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                matrix[i][j] = s.nextInt();
            }
        }

        System.out.println("Matrix:");
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
2 3  
1 2 3  
4 5 6  
```
**Output:**  
```
Matrix:  
1 2 3  
4 5 6  
```
---

### **137. Find the Diagonal Elements of a Matrix Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int[][] matrix = new int[n][n];

        for (int i = 0; i < n; i++)
            for (int j = 0; j < n; j++)
                matrix[i][j] = s.nextInt();

        System.out.println("Diagonal Elements:");
        for (int i = 0; i < n; i++)
            System.out.print(matrix[i][i] + " ");
    }
}
```
**Input:**  
```
3  
1 2 3  
4 5 6  
7 8 9  
```
**Output:**  
```
Diagonal Elements: 1 5 9  
```
---

### **138. Create a Number Grid Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                System.out.print(j + " ");
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
4
```
**Output:**  
```
1 2 3 4  
1 2 3 4  
1 2 3 4  
1 2 3 4  
```
---

### **139. Create a Star Pattern Like a Christmas Tree Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();

        // Printing the tree layers
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i + 1; j++) {
                for (int k = j; k < n + 1; k++) {
                    System.out.print(" ");
                }
                for (int k = 1; k <= (2 * j - 1); k++) {
                    System.out.print("*");
                }
                System.out.println();
            }
        }

        // Printing the tree trunk
        for (int i = 0; i < n / 2; i++) {
            for (int j = 0; j < n; j++) {
                if (j == n - 1) {
                    System.out.print("*");
                } else {
                    System.out.print(" ");
                }
            }
            System.out.println();
        }
    }
}
```
**Input:**  
```
5
```
**Output:**  
```
    *  
   ***  
  *****  
    *  
   ***  
  *****  
 ******  
    *  
   ***  
  *****  
 ******  
*********  
    *  
    *  
```
---

### **140. Perform Matrix Addition Using Nested Loops**  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        int[][] a = new int[n][n];
        int[][] b = new int[n][n];

        // Input first matrix
        for (int i = 0; i < n; i++)
            for (int j = 0; j < n; j++)
                a[i][j] = s.nextInt();

        // Input second matrix
        for (int i = 0; i < n; i++)
            for (int j = 0; j < n; j++)
                b[i][j] = s.nextInt();

        // Printing the sum of matrices
        System.out.println("Result:");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++)
                System.out.print((a[i][j] + b[i][j]) + " ");
            System.out.println();
        }
    }
}
```
**Input:**  
```
2  
1 2  
3 4  
5 6  
7 8  
```
**Output:**  
```
Result:  
6 8  
10 12  
```

### **41. Print a Fibonacci Sequence Using Recursion**
```java
import java.util.*;

public class Main {
    public static int fibonacci(int n) {
        if (n <= 1) return n;
        return fibonacci(n - 1) + fibonacci(n - 2);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for (int i = 0; i < n; i++)
            System.out.print(fibonacci(i) + " ");
    }
}
```

---

### **142. Implement a Switch Case That Calculates Tax Based on Income**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        double income = s.nextDouble();
        double tax = 0;

        switch ((int) income / 10000) {
            case 0, 1, 2: tax = 0; break;
            case 3, 4: tax = 0.05 * income; break;
            case 5, 6, 7: tax = 0.10 * income; break;
            default: tax = 0.15 * income;
        }
        System.out.println("Tax: " + tax);
    }
}
```

---

### **143. Generate Prime Numbers in a Given Range Using a Loop**
```java
import java.util.*;

public class Main {
    public static boolean isPrime(int n) {
        if (n < 2) return false;
        for (int i = 2; i * i <= n; i++)
            if (n % i == 0) return false;
        return true;
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int start = s.nextInt(), end = s.nextInt();

        for (int i = start; i <= end; i++)
            if (isPrime(i)) System.out.print(i + " ");
    }
}
```

---

### **144. Input Validation Program with a Loop**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num;

        while (true) {
            num = s.nextInt();
            if (num >= 1 && num <= 100) break;
            System.out.println("Invalid input, enter a number between 1 and 100:");
        }

        System.out.println("Valid input: " + num);
    }
}
```


### **146. Implement Binary Search in a Sorted Array**
```java
import java.util.*;

public class Main {
    public static int binarySearch(int[] arr, int key) {
        int left = 0, right = arr.length - 1;
        
        while (left <= right) {
            int mid = left + (right - left) / 2;
            if (arr[mid] == key) return mid;
            if (arr[mid] < key) left = mid + 1;
            else right = mid - 1;
        }
        return -1;
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt(), arr[] = new int[n];

        for (int i = 0; i < n; i++) arr[i] = s.nextInt();
        int key = s.nextInt();

        int result = binarySearch(arr, key);
        System.out.println(result == -1 ? "Not found" : "Found at index " + result);
    }
}
```

---

### **147. Implement Linear Search for a Number in an Array**
```java
import java.util.*;

public class Main {
    public static int linearSearch(int[] arr, int key) {
        for (int i = 0; i < arr.length; i++)
            if (arr[i] == key) return i;
        return -1;
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt(), arr[] = new int[n];

        for (int i = 0; i < n; i++) arr[i] = s.nextInt();
        int key = s.nextInt();

        int result = linearSearch(arr, key);
        System.out.println(result == -1 ? "Not found" : "Found at index " + result);
    }
}
```

---

### **148. Find the Largest Number Using a Method**
```java
import java.util.*;

public class Main {
    public static int findLargest(int[] arr) {
        int max = arr[0];
        for (int num : arr)
            if (num > max) max = num;
        return max;
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n = s.nextInt(), arr[] = new int[n];

        for (int i = 0; i < n; i++) arr[i] = s.nextInt();
        System.out.println("Largest: " + findLargest(arr));
    }
}
```

---

### **149. Count the Occurrence of Each Character in a String**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        String str = s.nextLine();
        int[] freq = new int[256];

        for (char c : str.toCharArray()) freq[c]++;
        for (int i = 0; i < 256; i++)
            if (freq[i] > 0) System.out.println((char) i + ": " + freq[i]);
    }
}
```



### **150. Perform Matrix Multiplication using Nested Loops**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int n1 = s.nextInt(), m1 = s.nextInt();
        int[][] mat1 = new int[n1][m1];
        for (int i = 0; i < n1; i++)
            for (int j = 0; j < m1; j++)
                mat1[i][j] = s.nextInt();

        int n2 = s.nextInt(), m2 = s.nextInt();
        int[][] mat2 = new int[n2][m2];
        for (int i = 0; i < n2; i++)
            for (int j = 0; j < m2; j++)
                mat2[i][j] = s.nextInt();

        if (m1 != n2) {
            System.out.println("Multiplication not possible");
            return;
        }

        int[][] result = new int[n1][m2];
        for (int i = 0; i < n1; i++)
            for (int j = 0; j < m2; j++)
                for (int k = 0; k < m1; k++)
                    result[i][j] += mat1[i][k] * mat2[k][j];

        for (int[] row : result) {
            for (int val : row)
                System.out.print(val + " ");
            System.out.println();
        }
    }
}
```

---

### **151. Implement a Stack using Control Flow Statements**
```java
import java.util.*;

public class Main {
    static int top = -1;
    static int[] stack = new int[5];

    public static void push(int val) {
        if (top == 4) {
            System.out.println("Stack Overflow");
            return;
        }
        stack[++top] = val;
    }

    public static void pop() {
        if (top == -1) {
            System.out.println("Stack Underflow");
            return;
        }
        System.out.println(stack[top--]);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        push(s.nextInt());
        push(s.nextInt());
        pop();
        pop();
        pop();
    }
}
```

---

### **152. Implement a Queue using Loops and Conditional Statements**
```java
import java.util.*;

public class Main {
    static int front = 0, rear = -1;
    static int[] queue = new int[5];

    public static void enqueue(int val) {
        if (rear == 4) {
            System.out.println("Queue Full");
            return;
        }
        queue[++rear] = val;
    }

    public static void dequeue() {
        if (front > rear) {
            System.out.println("Queue Empty");
            return;
        }
        System.out.println(queue[front++]);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        enqueue(s.nextInt());
        enqueue(s.nextInt());
        dequeue();
        dequeue();
        dequeue();
    }
}
```

---

### **153. Create a Simple Bank Account**
```java
import java.util.*;

public class Main {
    static double balance = 0;

    public static void deposit(double amount) {
        balance += amount;
    }

    public static void withdraw(double amount) {
        if (amount > balance) {
            System.out.println("Insufficient Balance");
        } else {
            balance -= amount;
        }
    }

    public static void checkBalance() {
        System.out.println("Balance: " + balance);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        deposit(s.nextDouble());
        withdraw(s.nextDouble());
        checkBalance();
    }
}
```

---

### **154. Simple Ticket Reservation System**
```java
import java.util.*;

public class Main {
    static int seats = 5;

    public static void bookTicket() {
        if (seats > 0) {
            seats--;
            System.out.println("Ticket Booked! Remaining: " + seats);
        } else {
            System.out.println("No Seats Available");
        }
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        for (int i = 0; i < 6; i++) bookTicket();
    }
}
```

---

### **155. Calculate Power Using Recursion**
```java
import java.util.*;

public class Main {
    public static int power(int base, int exp) {
        if (exp == 0) return 1;
        return base * power(base, exp - 1);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        System.out.println(power(s.nextInt(), s.nextInt()));
    }
}
```

---

### **156. Recursive Factorial Calculation**
```java
import java.util.*;

public class Main {
    public static long factorial(int n) {
        if (n == 0) return 1;
        return n * factorial(n - 1);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        System.out.println(factorial(s.nextInt()));
    }
}
```

---

### **157. Recursive Fibonacci Sequence**
```java
import java.util.*;

public class Main {
    public static int fibonacci(int n) {
        if (n <= 1) return n;
        return fibonacci(n - 1) + fibonacci(n - 2);
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        System.out.println(fibonacci(s.nextInt()));
    }
}
```

---

### **158. Number Guessing Game**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int target = (int) (Math.random() * 100) + 1, guess;

        while (true) {
            guess = s.nextInt();
            if (guess > target)
                System.out.println("Too High!");
            else if (guess < target)
                System.out.println("Too Low!");
            else {
                System.out.println("Correct!");
                break;
            }
        }
    }
}
```

---

### **159. Print Checkerboard Pattern**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int size = s.nextInt();

        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size; j++)
                System.out.print((i + j) % 2 == 0 ? "* " : "  ");
            System.out.println();
        }
    }
}
```

---

### **160. Vending Machine System Using Switch**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int choice = s.nextInt();

        switch (choice) {
            case 1: System.out.println("Dispensing Coffee"); break;
            case 2: System.out.println("Dispensing Tea"); break;
            case 3: System.out.println("Dispensing Soda"); break;
            default: System.out.println("Invalid Choice");
        }
    }
}
```


