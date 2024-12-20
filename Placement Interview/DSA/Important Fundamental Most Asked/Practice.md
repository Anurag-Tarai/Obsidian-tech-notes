```java
public class DayOfYear {
    public static void main(String[] args) {
        // Example inputs
        String date1 = "2019-01-09";
        String date2 = "2019-02-10";

        System.out.println(dayOfYear(date1)); // Output: 9
        System.out.println(dayOfYear(date2)); // Output: 41
    }

    public static int dayOfYear(String date) {
        // Split the input date into year, month, and day
        String[] parts = date.split("-");
        int year = Integer.parseInt(parts[0]);
        int month = Integer.parseInt(parts[1]);
        int day = Integer.parseInt(parts[2]);

        // Days in each month (for a common year)
        int[] daysInMonth = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};

        // Check if the given year is a leap year
        if (isLeapYear(year)) {
            daysInMonth[1] = 29; // February has 29 days in a leap year
        }

        // Sum up the days of the previous months
        int dayOfYear = 0;
        for (int i = 0; i < month - 1; i++) {
            dayOfYear += daysInMonth[i];
        }

        // Add the days of the current month
        dayOfYear += day;

        return dayOfYear;
    }

    // Function to check if a year is a leap year
    public static boolean isLeapYear(int year) {
        // A leap year is divisible by 4, but not by 100, unless also divisible by 400
        return (year % 4 == 0 && (year % 100 != 0 || year % 400 == 0));
    }
}

```

```java

// Function to perform right rotation using a for loop
public static void rotateRight(int[] arr, int n, int d) {
    // Temporary array to store rotated values
    int[] temp = new int[n];

    // Fill the temporary array with the rotated elements using the formula
    for (int i = 0; i < n; i++) {
        temp[(i + d) % n] = arr[i];  // Right rotate the index by d
    }

    // Copy the temporary array back to the original array
    for (int i = 0; i < n; i++) {
        arr[i] = temp[i];
    }
}


// Function to perform left rotation using a for loop
public static void rotateLeft(int[] arr, int n, int d) {
    // Temporary array to store rotated values
    int[] temp = new int[n];

    // Fill the temporary array with the rotated elements
    for (int i = 0; i < n; i++) {
        temp[i] = arr[(i + d) % n];  // Left rotate the index by d
    }

    // Copy the temporary array back to the original array
    for (int i = 0; i < n; i++) {
        arr[i] = temp[i];
    }
}


```

```java
public class AddStrings {
    public static String addDecimal(String num1, String num2) {
        StringBuilder result = new StringBuilder();
        int i = num1.length() - 1;
        int j = num2.length() - 1;
        int carry = 0;

        // Loop through both strings from right to left
        while (i >= 0 || j >= 0 || carry != 0) {
            // Get the current digit of num1 or 0 if no more digits are left
            int digit1 = (i >= 0) ? num1.charAt(i--) - '0' : 0;
            // Get the current digit of num2 or 0 if no more digits are left
            int digit2 = (j >= 0) ? num2.charAt(j--) - '0' : 0;
            
            // Add digits and carry
            int sum = digit1 + digit2 + carry;
            
            // Calculate new carry
            carry = sum / 10;
            
            // Append the current digit to the result
            result.append(sum % 10);
        }

        // Since we added digits from right to left, reverse the result
        return result.reverse().toString();
    }

    public static void main(String[] args) {
        String num1 = "123";
        String num2 = "456";
        System.out.println("Sum: " + addStrings(num1, num2));  // Output will be "579"
    }
}



public class AddBinary {
    public static String addBinary(String a, String b) {
        StringBuilder result = new StringBuilder();
        int i = a.length() - 1;
        int j = b.length() - 1;
        int carry = 0;

        // Loop through both strings from right to left
        while (i >= 0 || j >= 0 || carry != 0) {
            // Get the current digit of a or 0 if no more digits are left
            int digitA = (i >= 0) ? a.charAt(i--) - '0' : 0;
            // Get the current digit of b or 0 if no more digits are left
            int digitB = (j >= 0) ? b.charAt(j--) - '0' : 0;
            
            // Add digits and carry
            int sum = digitA + digitB + carry;
            
            // Calculate new carry (if sum is 2, carry will be 1, otherwise 0)
            carry = sum / 2;
            
            // Append the current binary digit to the result
            result.append(sum % 2);
        }

        // Since we added digits from right to left, reverse the result
        return result.reverse().toString();
    }

    public static void main(String[] args) {
        String a = "101";
        String b = "110";
        System.out.println("Sum: " + addBinary(a, b));  // Output will be "1011"
    }
}

```

```java
class AddBinary {
  public static void addBinary() {
    String a = "1010";
    String b = "1011";
    StringBuilder ans = new StringBuilder();
    int la = a.length() - 1;
    int lb = b.length() - 1;
    int carry = 0;
    while (la >= 0 || lb >= 0 || carry > 0) {
      int t1 = 0;
      int t2 = 0;
      if (la >= 0) {
        t1 = Character.getNumericValue(a.charAt(la));
        la--;
      }
      if (lb >= 0) {
        t2 = Character.getNumericValue(b.charAt(lb));
        lb--;
      }
      int addedValue = t1 + t2 + carry;
      ans.append("" + (addedValue % 2));
      carry = addedValue / 2;
    }
    System.out.println(ans.reverse().toString());
  }
}
```

```java
import java.util.Arrays;

class PlusOne {
  public static void plusOne(){
    int[] arr = {1,9,9,9};
    
    int addDigit = 1;
    int currentPosition = arr.length - 1;
    
    while(currentPosition>=0){
      String addValue = ""+(arr[currentPosition]+addDigit);
      if(addValue.length()==2){
        addDigit = Character.getNumericValue(addValue.charAt(0));
        arr[currentPosition] = Character.getNumericValue(addValue.charAt(1));
      }else{
        addDigit = 0;
        arr[currentPosition] = Integer.parseInt(addValue);
      }
      currentPosition--;
    }
    System.out.println(Arrays.toString(arr));
  }
}
```

```java
public class PrimeNumbersRecursion {

    public static void main(String[] args) {
        int N = 20; // Example: You can set N to any value
        System.out.println("Prime numbers less than or equal to " + N + ":");
        printPrimes(N);
    }

    // Function to print all prime numbers less than or equal to N
    static void printPrimes(int N) {
        if (N < 2) return; // Base case: No prime number less than 2
        printPrimes(N - 1); // Recursive call for N-1
        if (isPrime(N, 2)) {
            System.out.print(N + " ");
        }
    }

    // Helper function to check if a number is prime using recursion
    static boolean isPrime(int num, int divisor) {
        if (num <= 2) return num == 2; // 2 is prime; numbers <= 1 are not
        if (num % divisor == 0) return false; // Divisible by current divisor
        if (divisor * divisor > num) return true; // No divisors found
        return isPrime(num, divisor + 1); // Check next divisor
    }
}

```