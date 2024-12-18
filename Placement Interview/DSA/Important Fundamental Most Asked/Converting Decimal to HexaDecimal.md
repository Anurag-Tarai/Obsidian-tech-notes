```java
class Solution {

public String toHex(int num) {

if(num==0) return "0";

String value = "0123456789abcdef";

StringBuilder str = new StringBuilder();

long a = Integer.toUnsignedLong(num);

while(a>0){

str.append(value.charAt((int)(a%16)));

a/=16;

}

str.reverse();

return str.toString();

}

}
```