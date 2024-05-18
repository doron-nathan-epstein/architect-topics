# Bitwise Operators

Bitwise operators perform operations on the binary representations of integers. Here's a brief overview of the main bitwise operators in C#, along with simple examples and real-world use cases:

1. **AND (`&`)**:
   - **Description**: The bitwise AND operator compares each bit of its operands. If both bits are 1, the result is 1; otherwise, it is 0.
   - **Example**:

     ```csharp
     int a = 5;  // 0101 in binary
     int b = 3;  // 0011 in binary
     int result = a & b; // 0001 in binary, which is 1
     ```

   - **Real-world use case**: Checking if a specific bit is set. For instance, if you have a permission system where each bit represents a different permission, you can check if a user has a specific permission.

2. **OR (`|`)**:
   - **Description**: The bitwise OR operator compares each bit of its operands. If at least one of the bits is 1, the result is 1.
   - **Example**:

     ```csharp
     int a = 5;  // 0101 in binary
     int b = 3;  // 0011 in binary
     int result = a | b; // 0111 in binary, which is 7
     ```

   - **Real-world use case**: Setting specific bits. For example, setting multiple flags in a single integer.

3. **XOR (`^`)**:
   - **Description**: The bitwise XOR operator compares each bit of its operands. If the bits are different, the result is 1; otherwise, it is 0.
   - **Example**:

     ```csharp
     int a = 5;  // 0101 in binary
     int b = 3;  // 0011 in binary
     int result = a ^ b; // 0110 in binary, which is 6
     ```

   - **Real-world use case**: Flipping specific bits. For instance, toggling specific features on and off.

4. **NOT (`~`)**:
   - **Description**: The bitwise NOT operator inverts all the bits of its operand.
   - **Example**:

     ```csharp
     int a = 5;  // 0101 in binary
     int result = ~a; // 1010 in binary (in a 4-bit system, this would be -6 due to two's complement representation)
     ```

   - **Real-world use case**: Generating masks for bitwise operations or quickly calculating the bitwise complement of a number.

5. **Left Shift (`<<`)**:
   - **Description**: The left shift operator shifts the bits of its first operand to the left by the number of positions specified by its second operand. Bits shifted off to the left are discarded, and zeros are shifted in from the right.
   - **Example**:

     ```csharp
     int a = 5;  // 0101 in binary
     int result = a << 1; // 1010 in binary, which is 10
     ```

   - **Real-world use case**: Multiplying a number by a power of two. For instance, `a << 1` is equivalent to `a * 2`.

6. **Right Shift (`>>`)**:
   - **Description**: The right shift operator shifts the bits of its first operand to the right by the number of positions specified by its second operand. Bits shifted off to the right are discarded.
   - **Example**:

     ```csharp
     int a = 5;  // 0101 in binary
     int result = a >> 1; // 0010 in binary, which is 2
     ```

   - **Real-world use case**: Dividing a number by a power of two. For instance, `a >> 1` is equivalent to `a / 2`.

## Real-World Example: Setting and Checking Permissions

Consider a system where permissions are represented by bits in an integer:

- Read permission: 0b0001 (1)
- Write permission: 0b0010 (2)
- Execute permission: 0b0100 (4)

To set multiple permissions, you can use the OR operator:

```csharp
int permissions = 0;
permissions |= 1; // Add read permission
permissions |= 2; // Add write permission

// permissions now is 0b0011 (3), which means both read and write permissions are set.
```

To check if a specific permission is set, use the AND operator:

```csharp
bool hasReadPermission = (permissions & 1) != 0; // true if read permission is set
bool hasWritePermission = (permissions & 2) != 0; // true if write permission is set
bool hasExecutePermission = (permissions & 4) != 0; // true if execute permission is set
```

## Conclusion

Bitwise operators are powerful tools in programming, particularly useful in scenarios where you're working with low-level data, such as systems programming, network protocols, and hardware interfacing. Understanding these operators helps in optimizing code and managing binary data efficiently.
