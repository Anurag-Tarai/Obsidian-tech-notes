```java
class Solution {

public String toBinary(int num) {

if(num==0) return "0";

StringBuilder str = new StringBuilder();

long a = Integer.toUnsignedLong(num);

while(a>0){

str.append(((int)(a%2)));

a/=2;

}

str.reverse();

return str.toString();

}

}
```