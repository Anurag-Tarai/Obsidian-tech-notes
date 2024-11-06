## To find precision for floating point value
- precision refers to the number of digits after the decimal point.
```java
int a = 23.0234
System.out.printf("Formatted number: %.2f", number);

// using big decimal
BigDecimal number = new BigDecimal("123.456789"); 
BigDecimal roundedNumber = number.setScale(2, RoundingMode.HALF_UP);

// Define the precision using a format pattern 
DecimalFormat df = new DecimalFormat("#.##");
// Print the formatted number
System.out.println("Formatted number: " + df.format(number)); }
```
```