

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

**Input:**  
```
5
```
**Output:**  
```
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

