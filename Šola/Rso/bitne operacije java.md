`&` <- Bitwise AND. Sets each bit to 1 if both bits are 1.    a & b  
`|` <- Bitwise OR. Sets each bit to 1 if one of the bits is 1.  
`^` <- Bitwise XOR. Sets each bit to 1 if one of the bits is 1, but not both. a ^ b  
`~` <- Bitwise NOT. Inverts all the bits. ~a  
`<<` <- Left shift. Shifts bits to the left, filling with 0s.  a << 2  
`>>` <- Right shift. Shifts bits to the right, filling with the sign bit.   a >> 2  
`>>>` <- Unsigned right shift. Shifts bits to the right, filling with 0s.   a >>> 2  
`&=`  <- Bitwise AND with assignment. Performs a = a & b.   a &= b  
`|=` <- Bitwise OR with assignment. Performs a = a
`^=` <- Bitwise XOR with assignment. Performs a = a ^ b.   a ^= b  
`<<=` <- Left shift with assignment. Performs a = a << n.   a <<= 2  
`>>=` <- Right shift with assignment. Performs a = a >> n.  a >>= 2  
`>>>=` <- Unsigned right shift with assignment. Performs a = a >>> n.    a >>>= 2

1. **`&` (Bitwise AND)**
```java
byte a = 0b11010010;  // 210 in decimal
byte b = 0b10101100;  // 172 in decimal
byte result = (byte)(a & b);  // Result: 0b10000000 (128 in decimal)
```

2. **`|` (Bitwise OR)**
```java
byte a = 0b11010010;  // 210 in decimal
byte b = 0b10101100;  // 172 in decimal
byte result = (byte)(a | b);  // Result: 0b11111110 (254 in decimal)
```

3. **`^` (Bitwise XOR)**
```java
byte a = 0b11010010;  // 210 in decimal
byte b = 0b10101100;  // 172 in decimal
byte result = (byte)(a ^ b);  // Result: 0b01111110 (126 in decimal)
```

4. **`~` (Bitwise NOT)**
```java
byte a = 0b11010010;  // 210 in decimal
byte result = (byte)(~a);  // Result: 0b00101101 (-211 in decimal)
```

5. **`<<` (Left Shift)**
```java
byte a = 0b00000010;  // 2 in decimal
byte result = (byte)(a << 2);  // Result: 0b00001000 (8 in decimal)
```

6. **`>>` (Right Shift)**
```java
byte a = 0b11010010;  // 210 in decimal
byte result = (byte)(a >> 2);  // Result: 0b11110100 (52 in decimal)
```

7. **`>>>` (Unsigned Right Shift)**
```java
byte a = (byte)0b11010010;  // 210 in decimal
byte result = (byte)(a >>> 2);  // Result: 0b00110100 (52 in decimal)
```

8. **`&=` (Bitwise AND with assignment)**
```java
byte a = 0b11010010;  // 210 in decimal
byte b = 0b10101100;  // 172 in decimal
a &= b;  // Result: a = 0b10000000 (128 in decimal)
```

9. **`|=` (Bitwise OR with assignment)**
```java
byte a = 0b11010010;  // 210 in decimal
byte b = 0b10101100;  // 172 in decimal
a |= b;  // Result: a = 0b11111110 (254 in decimal)
```

10. **`^=` (Bitwise XOR with assignment)**
```java
byte a = 0b11010010;  // 210 in decimal
byte b = 0b10101100;  // 172 in decimal
a ^= b;  // Result: a = 0b01111110 (126 in decimal)
```

11. **`<<=` (Left shift with assignment)**
```java
byte a = 0b00000010;  // 2 in decimal
a <<= 2;  // Result: a = 0b00001000 (8 in decimal)
```

12. **`>>=` (Right shift with assignment)**
```java
byte a = 0b11010010;  // 210 in decimal
a >>= 2;  // Result: a = 0b11110100 (52 in decimal)
```

13. **`>>>=` (Unsigned right shift with assignment)**
```java
byte a = (byte)0b11010010;  // 210 in decimal
a >>>= 2;  // Result: a = 0b00110100 (52 in decimal)
```