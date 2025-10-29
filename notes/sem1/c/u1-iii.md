# Operators, Expressions, and I/O

## Statements and Expressions in C

In C, a **statement** is an instruction that tells the computer to perform a specific action. It ends with a semicolon (;). Examples include:

```c
int x = 10;
printf("Hello, World!");
return 0;
```

An **expression** is a combination of constants, variables, operators, and function calls that can be evaluated to produce a value. Examples include:

```c
int sum = 5 + 3; // 5 + 3 is an expression
int result = (x > y) ? x : y;  // ternary expression
```

Key differences:

- Statements perform actions; expressions produce values
- Some expressions can be statements (when they end with ;), but not all statements are expressions
- Examples of expressions:
  - Constants: 5, 3.14, 'a'
  - Variables: x, y
  - Function calls: printf("Hello")
  - Operations: 5 + 3, x * y
  - Composition: 5 + (x * y)

## Operators in C

### Binary and Unary Operators

**Binary operators** require two operands:

- Arithmetic: +, -, *, /, %
- Assignment: =, +=, -=, *=, /=, %=
- Comparison: ==, !=, >, <, >=, <=
- Logical: &&, ||, !
- Bitwise: &, |, ^, <<, >>

**Unary operators** require only one operand:

- Increment: ++ (pre and post)
- Decrement: -- (pre and post)
- Unary plus: +
- Unary minus: -
- Logical NOT: !
- Address of: &
- Indirection/dereference: *
- Size of: sizeof()

### Arithmetic Operators

The basic arithmetic operators are:

- Addition (+): Adds two operands
- Subtraction (-): Subtracts the second operand from the first
- Multiplication (*): Multiplies two operands
- Division (/): Divides the first operand by the second
- Modulus (%): Returns the remainder of division (only for integers)

```c
int a = 10, b = 5;
int sum = a + b;      // 15
int difference = a - b;  // 5
int product = a * b;    // 50
int quotient = a / b;   // 2
int remainder = a % b;  // 0
```

Important notes:

- Division of integers truncates toward zero
- Modulus operator cannot be applied to floating-point numbers
- The behavior of division and modulus with negative operands is implementation-defined in some cases according to the C standard

### Assignment Operators

Basic assignment: =

Compound assignment operators:

- `+=`: Add and assign
- `-=`: Subtract and assign
- `*=`: Multiply and assign
- `/=`: Divide and assign
- `%=`: Modulus and assign

```c
int x = 10;
x += 5;   // Equivalent to x = x + 5; (x becomes 15)
x *= 2;   // Equivalent to x = x * 2; (x becomes 30)
```

### Logical Operators

- `&&` (AND): Returns 1 (true) if both operands are non-zero
- `||` (OR): Returns 1 (true) if at least one operand is non-zero
- `!` (NOT): Returns 1 (true) if the operand is zero, otherwise returns 0 (false)

```c
int a = 1, b = 0;
int result1 = a && b;  // 0 (false)
int result2 = a || b;  // 1 (true)
int result3 = !a;      // 0 (false)
```

### Comparison Operators

- `==` (Equal to): Returns 1 if operands are equal
- `!=`kk (Not equal to): Returns 1 if operands are not equal
- `>` (Greater than): Returns 1 if first operand is greater than second
- `<` (Less than): Returns 1 if first operand is less than second
- `>=` (Greater than or equal to): Returns 1 if first operand is greater than or equal to second
- `<=` (Less than or equal to): Returns 1 if first operand is less than or equal to second

```c
int a = 10, b = 20;
int result1 = a > b;  // 0 (false)
int result2 = a < b;  // 1 (true)
int result3 = a == 10; // 1 (true)
```

### Bitwise Operators

- `&` (Bitwise AND): Performs bitwise AND operation
- `|` (Bitwise OR): Performs bitwise OR operation
- `^` (Bitwise XOR): Performs bitwise XOR operation
- `~` (Bitwise NOT): Inverts all bits of the operand
- `<<` (Left shift): Shifts bits to the left
- `>>` (Right shift): Shifts bits to the right

```c
int a = 5;  // 0101 in binary
int b = 3;  // 0011 in binary
int result1 = a & b;  // 0001 (1)
int result2 = a | b;  // 0111 (7)
int result3 = a ^ b;  // 0110 (6)
int result4 = ~a;     // -6 (two's complement)
int result5 = a << 1; // 1010 (10)
int result6 = a >> 1; // 0010 (2)
```

### Conditional Operator (Ternary Operator)

The conditional operator is the only ternary operator in C:
```c
condition ? expression1 : expression2
```

If `condition` is true (non-zero), `expression1` is evaluated; otherwise, `expression2` is evaluated.

```c
int x = 10, y = 5;
int max = (x > y) ? x : y;  // max becomes 10
```

## Order of Precedence of Operators

Operator precedence determines the grouping of operations in expressions. Higher precedence operators are evaluated before lower precedence ones.

| Precedence | Operator | Description |
|------------|----------|-------------|
| Highest    | () [] -> . | Function call, array subscript, member access |
|            | ++ -- - ! ~ * & sizeof | Unary operators, increment/decrement |
|            | * / % | Multiplicative operators |
|            | + - | Additive operators |
|            | << >> | Bitwise shifts |
|            | < <= > >= | Relational operators |
|            | == != | Equality operators |
|            | & | Bitwise AND |
|            | ^ | Bitwise XOR |
|            | \| | Bitwise OR |
|            | && | Logical AND |
|            | \|\| | Logical OR |
|            | ?: | Conditional operator |
|            | = += -= *= /= %= &= ^= <<= >>= | Assignment operators |
| Lowest     | , | Comma operator |

## Associativity of Operators

When operators have the same precedence, associativity determines the order of evaluation.

- **Left-to-right associativity**: Most operators have this

  - Arithmetic operators (+, -, *, /, %)
  - Bitwise operators (&, ^, |, <<, >>)
  - Relational operators (<, <=, >, >=)
  - Equality operators (==, !=)
  - Assignment operators (=, +=, etc.)

- **Right-to-left associativity**:

  - Unary operators (!, ~, ++, --, *, &)
  - Conditional operator (? :)
  - Assignment operators

Example of associativity:
```c
int a = 10, b = 20, c = 30;
int result = a + b + c;  // Left-to-right: ((a + b) + c)

int x = 5, y, z;
y = z = x;  // Right-to-left: y = (z = x)
```

## Typecasting

Typecasting is the explicit conversion of a value from one data type to another.

### Implicit Type Conversion

When mixing data types in expressions, C performs implicit type promotion:

1. If one operand is float, the other is converted to float
2. If one operand is double, the other is converted to double
3. If one operand is long, the other is converted to long
4. Otherwise, both operands are converted to int

```c
int a = 5;
float b = 2.0;
float result = a / b;  // Both operands promoted to float
```

### Explicit Type Conversion

Syntax: `(target_type) expression`

```c
int a = 7;
float b = 2.0;
int result = (int) (a / b);  // 3.5 becomes 3 ( truncation )
```

Common casts:

- Cast to larger type (widening): preserves information, may add zeros
- Cast to smaller type (narrowing): potential loss of data

## Input and Output Statements

### getchar(), getc(), getch()

- **getchar()**: Reads a single character from the standard input (usually keyboard).
  ```c
  int c = getchar();
  ```

- **getc()**: Similar to getchar() but can read from any specified stream.
  ```c
  int c = getc(stdin);  // Equivalent to getchar()
  int c = getc(file);    // Read from a file
  ```

- **getch()**: Non-standard function (commonly in <conio.h> for Windows) that reads a character without displaying it on the screen (no echo).
  ```c
  int c = getch();
  ```

### putchar(), putc(), puts()

- **putchar()**: Writes a single character to the standard output (usually the screen).
  ```c
  putchar('A');
  ```

- **putc()**: Similar to putchar() but can write to any specified stream.
  ```c
  putc('A', stdout);  // Equivalent to putchar('A')
  putc('A', file);     // Write to a file
  ```

- **puts()**: Writes a string to the standard output, followed by a newline character.
  ```c
  puts("Hello, World!");
  ```

### scanf(), printf()

- **scanf()**: Reads formatted input from the standard input.
  ```c
  int age;
  float salary;
  scanf("%d %f", &age, &salary);
  ```

- **printf()**: Writes formatted output to the standard output.
  ```c
  int age = 25;
  printf("Age: %d", age);
  ```

Both functions use format specifiers to control how data is read or written.

### Format Specifiers

Common format specifiers:

| Specifier | Data Type | Description |
|-----------|-----------|-------------|
| %d, %i    | int       | Signed decimal integer |
| %u        | unsigned int | Unsigned decimal integer |
| %f, %F    | float     | Decimal floating point |
| %e, %E    | float     | Scientific notation |
| %g, %G    | float     | Uses %f or %e, whichever is shorter |
| %c        | char      | Single character |
| %s        | char*     | String of characters |
| %p        | void*     | Pointer address |
| %x, %X    | int       | Hexadecimal integer |
| %o        | int       | Octal integer |
| %%        | -         | Literal '%' character |

Additional flags for format specifiers:

| Flag | Description |
|------|-------------|
| -    | Left justify |
| +    | Always print sign (+ or -) |
| 0    | Pad with zeros |
| #    | Alternative form (for example, 0x prefix for hex) |
| width | Minimum number of characters to be printed |
| .prec | Precision for floats or maximum characters to be printed for strings |

Examples:
```c
int age = 25;
float height = 5.9;
char name[] = "Alice";

printf("Name: %10s", name);      // Right-aligned, 10 chars wide
printf("Name: %-10s", name);     // Left-aligned, 10 chars wide
printf("Height: %07.2f", height); // Zero padded, 7 chars wide, 2 decimal places
printf("Age: %d (+/- %d)", age, age); // Multiple format specifiers
```
