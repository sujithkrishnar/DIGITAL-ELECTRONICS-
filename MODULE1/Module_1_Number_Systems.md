**MODULE 1**

**NUMBER SYSTEMS**

**Learning Objectives**

After completing this module, you should be able to:

- Explain decimal, binary, octal and hexadecimal number systems.
- Explain positional notation and the radix/base concept.
- Identify the MSB and LSB of a binary value.
- Represent integer and fractional values in different bases.
- Convert integers and fractions between common number systems.
- Use direct binary-to-octal and binary-to-hexadecimal grouping.
- Calculate numerical ranges for fixed-width integers.
- Explain overflow and underflow with simple examples.
- Understand how binary representation connects to digital circuits and computer hardware.

# Quick Number-System Overview

| **System**  | **Base** | **Valid symbols** | **Binary relationship**            | **Common use**                        |
| ----------- | -------- | ----------------- | ---------------------------------- | ------------------------------------- |
| Decimal     | 10       | 0–9               | Human-readable values              | Everyday mathematics and input/output |
| Binary      | 2        | 0–1               | Fundamental digital representation | Computers and digital circuits        |
| Octal       | 8        | 0–7               | 1 digit = 3 bits                   | Unix permissions and legacy systems   |
| Hexadecimal | 16       | 0–9, A–F          | 1 digit = 4 bits                   | Memory, debugging, colors, networking |

# 1\. 1 Decimal Number System

## What is it?

Decimal is the number system used in normal everyday counting and mathematics. It is called base 10 because it has ten possible digits: 0 through 9. A decimal number can contain an integer part and, when needed, a fractional part.

## How does it work?

Decimal is positional. The position immediately to the left of the decimal point has weight 10^0, the next has weight 10^1, then 10^2, and so on. Positions to the right use negative powers such as 10^-1 and 10^-2.

## Formula / Rule

Integer value = Σ(digit × 10^position). For fractional positions, the position is negative.

## Step-by-step example: 583₁₀

1\. Write the place values: 5×10², 8×10¹, 3×10⁰.  
2\. Calculate: 500 + 80 + 3.  
3\. Add: 583.

## Where is it used in computers / programming?

- Programming languages normally display ordinary integer values in decimal notation.
- Decimal is commonly used for user input, output, counters, measurements and database values.

## Real-world applications

- Money and prices
- Age, distance, weight and temperature
- School marks and percentages
- Scientific measurements

## Key points / exam notes

- Base = 10.
- Valid digits = 0 to 9.
- Every position has a power-of-10 weight.
- The digit's value depends on both the digit and its position.

# 1\. 2 Binary Number System

## What is it?

Binary is a base-2 number system that uses only 0 and 1. A single binary digit is called a bit. Digital computers use binary because electronic circuits can reliably represent two logical states.

## How does it work?

Each position has a power-of-2 weight. Starting at the binary point, the first position to the left is 2^0, then 2^1, 2^2, etc. To the right are 2^-1, 2^-2, etc.

## Formula / Rule

Binary value = Σ(bit × 2^position).

## Step-by-step example: 101101₂

1\. Assign weights: 2^5, 2^4, 2^3, 2^2, 2^1, 2^0.  
2\. Multiply: 32, 16, 0, 4, 0, 1.  
3\. Add: 32 + 16 + 4 + 1 = 53.  
Therefore, 101101₂ = 53₁₀.

### Binary place-value table

| **Bit position** | **Power of 2** | **Weight** |
| ---------------- | -------------- | ---------- |
| 0                | 2^0            | 1          |
| 1                | 2^1            | 2          |
| 2                | 2^2            | 4          |
| 3                | 2^3            | 8          |
| 4                | 2^4            | 16         |
| 5                | 2^5            | 32         |
| 6                | 2^6            | 64         |
| 7                | 2^7            | 128        |

## Where is it used in computers / programming?

- CPU registers and memory store information as bit patterns.
- Machine instructions, flags and bitwise operations are represented using binary.
- Digital sensors and microcontrollers often convert physical states into binary data.

## Real-world applications

- ON/OFF switching
- Digital communication
- Electronic control systems
- Computers, phones and embedded devices

## Key points / exam notes

- Base = 2.
- Valid digits = 0 and 1.
- One binary digit = one bit.
- Binary is the fundamental representation used by digital hardware.

# 1\. 3 Octal Number System

## What is it?

Octal is a base-8 number system. It uses eight symbols: 0 through 7. It was useful historically because it provides a compact representation of binary values.

## How does it work?

Each octal position has a power-of-8 weight. There is also a direct binary relationship: every octal digit maps to exactly three binary bits.

## Formula / Rule

Octal value = Σ(digit × 8^position).

## Step-by-step example: 725₈

1\. Expand: 7×8² + 2×8¹ + 5×8⁰.  
2\. Calculate: 7×64 + 2×8 + 5.  
3\. Add: 448 + 16 + 5 = 469.  
Therefore, 725₈ = 469₁₀.

### Octal to binary table

| **Octal** | **Binary** |
| --------- | ---------- |
| 0         | 000        |
| 1         | 001        |
| 2         | 010        |
| 3         | 011        |
| 4         | 100        |
| 5         | 101        |
| 6         | 110        |
| 7         | 111        |

## Where is it used in computers / programming?

- Unix/Linux permissions are commonly written in octal, such as 755.
- Octal appears in some legacy and low-level computing contexts.

## Real-world applications

- Unix file permissions
- Legacy computer systems
- Some embedded and low-level representations

## Key points / exam notes

- Base = 8.
- Valid digits = 0–7.
- One octal digit corresponds to 3 binary bits.
- 8 and 9 are invalid octal digits.

# 1\. 4 Hexadecimal Number System

## What is it?

Hexadecimal is a base-16 system. Because ten digits are not enough, it uses A–F for decimal values 10–15.

## How does it work?

Each position has a power-of-16 weight. Hexadecimal is especially useful because four binary bits correspond exactly to one hexadecimal digit.

## Formula / Rule

Hex value = Σ(digit × 16^position).

## Step-by-step example: 2AF₁₆

1\. Replace A with 10 and F with 15.  
2\. Expand: 2×16² + 10×16¹ + 15×16⁰.  
3\. Calculate: 512 + 160 + 15 = 687.  
Therefore, 2AF₁₆ = 687₁₀.

### Hexadecimal digit table

| **Hex** | **Decimal** | **4-bit binary** |
| ------- | ----------- | ---------------- |
| 0       | 0           | 0000             |
| 1       | 1           | 0001             |
| 2       | 2           | 0010             |
| 3       | 3           | 0011             |
| 4       | 4           | 0100             |
| 5       | 5           | 0101             |
| 6       | 6           | 0110             |
| 7       | 7           | 0111             |
| 8       | 8           | 1000             |
| 9       | 9           | 1001             |
| A       | 10          | 1010             |
| B       | 11          | 1011             |
| C       | 12          | 1100             |
| D       | 13          | 1101             |
| E       | 14          | 1110             |
| F       | 15          | 1111             |

## Where is it used in computers / programming?

- Memory addresses and machine-code values are often displayed in hexadecimal.
- Debuggers and programmers use hexadecimal to inspect raw bytes and bit patterns.
- HTML/CSS color values use hexadecimal notation such as #FF0000.

## Real-world applications

- Web colors
- MAC addresses
- IPv6 addresses
- Embedded systems
- Debugging and memory inspection

## Key points / exam notes

- Base = 16.
- Valid symbols = 0–9 and A–F.
- A=10, B=11, C=12, D=13, E=14, F=15.
- One hexadecimal digit represents 4 bits.

# 1\. 5 Positional Notation

## What is it?

Positional notation means that a digit's value depends on where it appears in a number. The same symbol can have different values in different positions.

## How does it work?

The rightmost integer position has power 0. Moving left increases the power by one. Moving right of the radix point uses negative powers.

## Formula / Rule

Value = Σ(digit × base^position).

## Step-by-step example: 321₄

1\. Write weights: 4², 4¹, 4⁰.  
2\. Calculate: 3×16 + 2×4 + 1×1.  
3\. Add: 48 + 8 + 1 = 57.  
Therefore, 321₄ = 57₁₀.

## Where is it used in computers / programming?

- All positional number systems are used in computer data representation and conversion.
- Understanding positional notation makes base conversion and binary arithmetic easier.

## Real-world applications

- Counting systems
- Digital data representation
- Computer arithmetic

## Key points / exam notes

- Position determines place value.
- The rightmost integer position has power 0.
- The same digit can represent different values in different positions.

# 1\. 6 Radix / Base Concept

## What is it?

Radix, or base, is the number of distinct symbols used by a positional number system. Binary has radix 2, decimal has radix 10, octal has radix 8 and hexadecimal has radix 16.

## How does it work?

The base determines the place-value weights. For base B, the integer positions are B⁰, B¹, B², B³ and so on.

## Formula / Rule

Place value = B^position.

## Step-by-step example: 101₂

1\. Base is 2.  
2\. Expand: 1×2² + 0×2¹ + 1×2⁰.  
3\. Result = 4 + 0 + 1 = 5₁₀.

### Base comparison

| **Number system** | **Base** | **Valid digits** |
| ----------------- | -------- | ---------------- |
| Binary            | 2        | 0–1              |
| Octal             | 8        | 0–7              |
| Decimal           | 10       | 0–9              |
| Hexadecimal       | 16       | 0–9, A–F         |

## Where is it used in computers / programming?

- Base determines how a value is interpreted during conversion.
- Programming languages use prefixes or notation conventions to identify binary, octal and hexadecimal literals.

## Real-world applications

- Different counting and coding systems
- Digital and computer data representation

## Key points / exam notes

- Radix = base.
- A base B system has B possible symbols.
- No digit can be equal to or greater than the base.

# 1\. 7 MSB and LSB

## What is it?

MSB means Most Significant Bit and normally refers to the leftmost bit in a binary representation. LSB means Least Significant Bit and normally refers to the rightmost bit.

## How does it work?

The MSB carries the largest positional weight in an unsigned binary integer, while the LSB carries the smallest weight, 2⁰ = 1.

## Formula / Rule

MSB weight for an n-bit unsigned value = 2^(n−1). LSB weight = 2⁰ = 1.

## Step-by-step example: 101101₂

The MSB is the first 1 on the left. Its weight is 2⁵ = 32. The LSB is the final 1 on the right. Its weight is 2⁰ = 1.

## Where is it used in computers / programming?

- Bit shifting and masking often refer to the most or least significant bits.
- Serial communication protocols may transmit bits in MSB-first or LSB-first order.
- The LSB is commonly used in parity and bit-level operations.

## Real-world applications

- Digital communication
- Microcontrollers
- Binary sensors
- Data serialization

## Key points / exam notes

- MSB = most significant bit.
- LSB = least significant bit.
- MSB is normally leftmost; LSB is normally rightmost.
- Always check the stated bit order when dealing with communication protocols.

# 1\. 8 Integer Representation

## What is it?

Integer representation describes how whole numbers are stored using a fixed number of bits. The two broad categories are unsigned and signed representation.

## How does it work?

Unsigned representation uses every bit for magnitude. Signed representations reserve information for negative values. Modern systems commonly use two's complement for signed integers.

## Formula / Rule

Unsigned n-bit range: 0 to 2^n−1. Signed two's-complement n-bit range: −2^(n−1) to 2^(n−1)−1.

## Step-by-step example: represent 25 using 8 bits

1\. Convert 25 to binary: 11001.  
2\. Add leading zeros to make 8 bits.  
3\. Result: 00011001₂.

### Common signed representations

| **Method**       | **Main idea**                                          | **Comment**                      |
| ---------------- | ------------------------------------------------------ | -------------------------------- |
| Sign-magnitude   | One bit indicates sign; remaining bits store magnitude | Simple concept but has +0 and −0 |
| One's complement | Negative value formed by inverting bits                | Also has two zeros               |
| Two's complement | Invert bits and add 1                                  | Common modern representation     |

## Where is it used in computers / programming?

- Programming integer types such as byte, short, int and long use fixed-width representations.
- CPU registers store integer bit patterns.
- Array indexes, counters and arithmetic operations depend on integer representation.

## Real-world applications

- Digital counters
- Embedded controllers
- Software variables
- Processor arithmetic

## Key points / exam notes

- Unsigned n-bit range = 0 to 2^n−1.
- Signed two's-complement n-bit range = −2^(n−1) to 2^(n−1)−1.
- Leading zeros do not change an unsigned integer's value.

# 1\. 9 Fractional Representation

## What is it?

A fractional number has digits to the right of a radix point. In decimal, those positions use negative powers of 10.

## How does it work?

Starting immediately to the right of the point, the weights are base^-1, base^-2, base^-3 and so on.

## Formula / Rule

Fractional value = Σ(digit × base^negative_position).

## Step-by-step example: 25.75₁₀

1\. Integer part: 2×10¹ + 5×10⁰ = 25.  
2\. Fractional part: 7×10⁻¹ + 5×10⁻² = 0.7 + 0.05.  
3\. Total = 25.75.

## Where is it used in computers / programming?

- Floating-point data types represent many fractional values.
- Scientific and engineering software uses fractional representations for measurements and calculations.

## Real-world applications

- Temperature
- Measurements
- Scientific calculations
- Financial values

## Key points / exam notes

- Positions after the radix point use negative powers.
- The first fractional position is base^-1.
- Integer and fractional parts can be converted separately.

# 1\. 10 Binary Fractions

## What is it?

A binary fraction is a number containing a binary point, such as 101.101₂. The positions after the binary point use negative powers of 2.

## How does it work?

The first fractional bit has weight 2^-1 = 0.5, the next has 2^-2 = 0.25, then 2^-3 = 0.125, and so on.

## Formula / Rule

Binary fractional value = Σ(bit × 2^negative_position).

## Step-by-step example: 0.101₂

1\. First bit: 1×2^-1 = 0.5.  
2\. Second bit: 0×2^-2 = 0.  
3\. Third bit: 1×2^-3 = 0.125.  
4\. Add: 0.625.  
Therefore, 0.101₂ = 0.625₁₀.

### Binary fractional weights

| **Position** | **Power** | **Value** |
| ------------ | --------- | --------- |
| 1st          | 2^-1      | 0.5       |
| 2nd          | 2^-2      | 0.25      |
| 3rd          | 2^-3      | 0.125     |
| 4th          | 2^-4      | 0.0625    |
| 5th          | 2^-5      | 0.03125   |

## Where is it used in computers / programming?

- Floating-point hardware ultimately stores values in binary-based formats.
- Binary fractions are important when studying floating-point precision and numerical error.

## Real-world applications

- Scientific computing
- Digital signal processing
- Graphics and simulations

## Key points / exam notes

- First bit after the binary point has weight 1/2.
- Not every decimal fraction has a finite binary representation.
- Separate integer and fractional parts when converting mixed values.

# 1\. 11 Decimal-to-Binary Conversion

## What is it?

For a positive integer, decimal-to-binary conversion is performed by repeatedly dividing by 2 and recording the remainders.

## How does it work?

Each division removes one binary place. The final quotient becomes zero. Because the first remainder is the least significant bit, the remainders are read from bottom to top.

## Formula / Rule

Repeatedly divide by 2; record remainder 0 or 1; read remainders in reverse order.

## Step-by-step example: 25₁₀ → binary

25 ÷ 2 = 12 remainder 1  
12 ÷ 2 = 6 remainder 0  
6 ÷ 2 = 3 remainder 0  
3 ÷ 2 = 1 remainder 1  
1 ÷ 2 = 0 remainder 1  
Read bottom to top: 11001₂.  
Therefore, 25₁₀ = 11001₂.

### Conversion checklist

| **Step** | **Action**                         |
| -------- | ---------------------------------- |
| 1        | Divide the decimal number by 2     |
| 2        | Write the remainder                |
| 3        | Divide the quotient again          |
| 4        | Continue until quotient becomes 0  |
| 5        | Read remainders from bottom to top |

## Where is it used in computers / programming?

- Useful when manually interpreting binary values from decimal data.
- Important for understanding how integers are represented in memory and registers.

## Real-world applications

- Digital design calculations
- Programming exercises
- Computer architecture studies

## Key points / exam notes

- Use division by 2 for integer conversion.
- Read remainders from bottom to top.
- Do not read them in the same order they were produced.

# 1\. 12 Binary-to-Decimal Conversion

## What is it?

Binary-to-decimal conversion uses positional weights of powers of 2.

## How does it work?

Start with the rightmost bit at 2⁰. Move left and increase the power by one. Multiply each bit by its weight and add the results.

## Formula / Rule

Decimal value = Σ(bit × 2^position).

## Step-by-step example: 110101₂ → decimal

1\. Weights: 32, 16, 8, 4, 2, 1.  
2\. Multiply: 1×32 + 1×16 + 0×8 + 1×4 + 0×2 + 1×1.  
3\. Add: 32 + 16 + 4 + 1 = 53.  
Therefore, 110101₂ = 53₁₀.

### Worked table

| **Bit** | **Weight** | **Contribution** |
| ------- | ---------- | ---------------- |
| 1       | 32         | 32               |
| 1       | 16         | 16               |
| 0       | 8          | 0                |
| 1       | 4          | 4                |
| 0       | 2          | 0                |
| 1       | 1          | 1                |

## Where is it used in computers / programming?

- Useful for reading binary data shown by debuggers, hardware tools and bitwise operations.

## Real-world applications

- Digital electronics calculations
- Network and hardware troubleshooting

## Key points / exam notes

- Use powers of 2.
- The rightmost bit always has weight 1 for an integer.
- Add only the weights corresponding to 1 bits.

# 1\. 13 Decimal-to-Octal Conversion

## What is it?

Decimal-to-octal integer conversion uses repeated division by 8.

## How does it work?

Each remainder is one octal digit. The remainders are read from bottom to top.

## Formula / Rule

Repeatedly divide by 8; record remainders; read bottom to top.

## Step-by-step example: 100₁₀ → octal

100 ÷ 8 = 12 remainder 4  
12 ÷ 8 = 1 remainder 4  
1 ÷ 8 = 0 remainder 1  
Read bottom to top: 144₈.  
Therefore, 100₁₀ = 144₈.

## Where is it used in computers / programming?

- Octal may appear when working with Unix/Linux permission modes or older low-level systems.

## Real-world applications

- Unix/Linux file permissions
- Legacy computing

## Key points / exam notes

- Divide by 8.
- Valid remainders are 0–7.
- Read remainders from bottom to top.

# 1\. 14 Octal-to-Decimal Conversion

## What is it?

Octal-to-decimal conversion expands each octal digit using powers of 8.

## How does it work?

Starting from the rightmost digit, assign 8⁰, 8¹, 8² and so on.

## Formula / Rule

Decimal value = Σ(octal digit × 8^position).

## Step-by-step example: 157₈ → decimal

1\. Expand: 1×8² + 5×8¹ + 7×8⁰.  
2\. Calculate: 64 + 40 + 7.  
3\. Add: 111.  
Therefore, 157₈ = 111₁₀.

## Where is it used in computers / programming?

- Useful for interpreting octal permission values and legacy representations.

## Real-world applications

- Unix permissions
- Legacy data formats

## Key points / exam notes

- Use powers of 8.
- No octal digit can be 8 or 9.

# 1\. 15 Decimal-to-Hexadecimal Conversion

## What is it?

Decimal-to-hexadecimal conversion of an integer uses repeated division by 16.

## How does it work?

When a remainder is 10–15, replace it with A–F. Read the remainders from bottom to top.

## Formula / Rule

Repeatedly divide by 16; convert remainders 10–15 to A–F; read bottom to top.

## Step-by-step example: 254₁₀ → hexadecimal

254 ÷ 16 = 15 remainder 14.  
15 ÷ 16 = 0 remainder 15.  
14 = E and 15 = F.  
Read bottom to top: FE₁₆.  
Therefore, 254₁₀ = FE₁₆.

## Where is it used in computers / programming?

- Hexadecimal is commonly used to display bytes, memory addresses and debugging information.

## Real-world applications

- Web colors
- Memory addresses
- Networking identifiers

## Key points / exam notes

- Divide by 16.
- Remainders 10–15 become A–F.
- Read remainders from bottom to top.

# 1\. 16 Hexadecimal-to-Decimal Conversion

## What is it?

Hexadecimal-to-decimal conversion expands each digit using powers of 16.

## How does it work?

Convert letters A–F to decimal values first. Then multiply each digit by the corresponding power of 16 and add.

## Formula / Rule

Decimal value = Σ(hex digit value × 16^position).

## Step-by-step example: 2B₁₆ → decimal

B = 11.  
2×16¹ + 11×16⁰ = 32 + 11 = 43.  
Therefore, 2B₁₆ = 43₁₀.

## Where is it used in computers / programming?

- Used to interpret hexadecimal values shown by debuggers, memory viewers and programming documentation.

## Real-world applications

- Color codes
- Network addresses
- Hardware identifiers

## Key points / exam notes

- A=10 through F=15.
- Use powers of 16.
- Rightmost integer digit has weight 16⁰.

# 1\. 17 Binary-to-Octal Conversion

## What is it?

Binary-to-octal conversion can be done directly because 8 = 2³. Therefore, every group of three binary bits corresponds to one octal digit.

## How does it work?

Starting from the binary point, group integer bits in sets of three from right to left. If the leftmost group is incomplete, add leading zeros. For fractions, group from the point toward the right and add trailing zeros if necessary.

## Formula / Rule

1 octal digit = 3 binary bits.

## Step-by-step example: 110101₂ → octal

1\. Group from the right: 110 101.  
2\. Convert 110 → 6.  
3\. Convert 101 → 5.  
4\. Therefore, 110101₂ = 65₈.

## Where is it used in computers / programming?

- Provides a compact representation of binary values in contexts where octal is used.

## Real-world applications

- Unix permission notation
- Legacy computing

## Key points / exam notes

- Group 3 bits.
- Group from the radix point outward.
- Leading zeros may be added to complete an integer group.

# 1\. 18 Octal-to-Binary Conversion

## What is it?

Octal-to-binary conversion is the reverse of binary-to-octal conversion. Every octal digit becomes exactly three binary bits.

## How does it work?

Use the octal-to-binary lookup table and concatenate the groups without changing their order.

## Formula / Rule

1 octal digit = 3 binary bits.

## Step-by-step example: 57₈ → binary

1\. 5 maps to 101.  
2\. 7 maps to 111.  
3\. Join them: 101111.  
Therefore, 57₈ = 101111₂.

## Where is it used in computers / programming?

- Useful for quickly expanding octal values into bit patterns.

## Real-world applications

- Unix permissions and legacy representations

## Key points / exam notes

- Each octal digit always maps to exactly 3 bits.
- Do not reverse the bit order.

# 1\. 19 Binary-to-Hexadecimal Conversion

## What is it?

Binary-to-hexadecimal conversion is direct because 16 = 2⁴. Every four binary bits form one hexadecimal digit.

## How does it work?

Group integer bits into sets of four from right to left. Add leading zeros if necessary. For fractional values, group from the binary point outward.

## Formula / Rule

1 hexadecimal digit = 4 binary bits.

## Step-by-step example: 10101111₂ → hexadecimal

1\. Group: 1010 1111.  
2\. 1010 = A.  
3\. 1111 = F.  
4\. Therefore, 10101111₂ = AF₁₆.

## Where is it used in computers / programming?

- Hexadecimal is a convenient human-readable form of binary bytes and machine data.

## Real-world applications

- Debugging
- Memory inspection
- Web colors
- Networking

## Key points / exam notes

- Group 4 bits.
- Use the 4-bit hexadecimal table.
- Do not convert through decimal unless required.

# 1\. 20 Hexadecimal-to-Binary Conversion

## What is it?

Hexadecimal-to-binary conversion replaces each hexadecimal symbol with its 4-bit binary equivalent.

## How does it work?

Convert each digit independently and concatenate the four-bit groups.

## Formula / Rule

1 hexadecimal digit = 4 binary bits.

## Step-by-step example: 3C₁₆ → binary

1\. 3 = 0011.  
2\. C = 1100.  
3\. Join: 00111100.  
Therefore, 3C₁₆ = 00111100₂.

## Where is it used in computers / programming?

- Useful when analyzing bytes, bit flags, machine code and network data.

## Real-world applications

- Memory dumps
- Network packet analysis
- Microcontroller programming

## Key points / exam notes

- Each hexadecimal digit maps to four bits.
- Keep leading zeros inside each 4-bit group when showing a byte or fixed-width value.

# 1\. 21 Mixed-Radix Conversions

## What is it?

Mixed-radix conversion means moving through or working with values represented in different bases. A common path is binary → decimal → hexadecimal, although direct conversions are often faster.

## How does it work?

Use the conversion method appropriate to each step. Binary-to-octal and binary-to-hexadecimal can be performed directly using bit grouping because their bases are powers of 2.

## Formula / Rule

Common direct relationships: 8 = 2³ and 16 = 2⁴.

## Step-by-step example: 1010₂ → hexadecimal

Method 1: Binary → Decimal → Hex.  
1010₂ = 10₁₀, and 10₁₀ = A₁₆.  
Method 2: Direct grouping.  
1010 is one 4-bit group, which maps directly to A.  
Therefore, 1010₂ = A₁₆.

## Where is it used in computers / programming?

- Used when converting values between programmer-friendly representations.
- Direct binary/hex conversion is common in debugging and hardware work.

## Real-world applications

- Data analysis
- Debugging
- Digital electronics

## Key points / exam notes

- Choose the shortest valid conversion path.
- Binary ↔ octal uses 3-bit groups.
- Binary ↔ hexadecimal uses 4-bit groups.

# 1\. 22 Conversion of Fractional Numbers

## What is it?

Fractional conversion handles digits after the radix point. Integer and fractional parts use different algorithms.

## How does it work?

For decimal fraction → binary, repeatedly multiply the fractional part by 2. The integer part of each result becomes the next binary fractional bit. For conversion from binary to decimal, use negative powers of 2.

## Formula / Rule

Decimal fraction → target base: repeatedly multiply by the target base and record the integer parts.

## Step-by-step example: 10.625₁₀ → binary

Integer part: 10₁₀ = 1010₂.  
Fractional part:  
0.625×2 = 1.250 → 1  
0.250×2 = 0.500 → 0  
0.500×2 = 1.000 → 1  
So 0.625₁₀ = 0.101₂.  
Final answer: 10.625₁₀ = 1010.101₂.

## Where is it used in computers / programming?

- Fractional conversion is important for understanding floating-point representation and precision.

## Real-world applications

- Measurements
- Scientific calculations
- Graphics
- Signal processing

## Key points / exam notes

- Convert integer and fraction separately.
- For decimal fraction → binary, multiply by 2.
- Read the generated integer parts from top to bottom.

# 1\. 23 Numerical Range

## What is it?

Numerical range is the set of values that can be represented with a fixed number of bits. The range depends on whether the representation is signed or unsigned.

## How does it work?

For n-bit unsigned integers, all bits represent magnitude. For n-bit two's-complement integers, one half of the possible patterns represent negative values and the other half represent non-negative values.

## Formula / Rule

Unsigned: 0 to 2^n−1. Signed two's complement: −2^(n−1) to 2^(n−1)−1.

## Step-by-step example: 8-bit range

Unsigned: 2^8−1 = 255, so 0 to 255.  
Signed two's complement: minimum −2^7 = −128 and maximum 2^7−1 = 127.

### Range reference

| **Bits** | **Unsigned range** | **Signed two's-complement range** |
| -------- | ------------------ | --------------------------------- |
| 4        | 0 to 15            | −8 to 7                           |
| 8        | 0 to 255           | −128 to 127                       |
| 16       | 0 to 65,535        | −32,768 to 32,767                 |
| 32       | 0 to 4,294,967,295 | −2^31 to 2^31−1                   |

## Where is it used in computers / programming?

- Helps programmers select appropriate integer data types.
- Determines whether a value fits inside a register, memory field or database column.
- Important in embedded systems where memory width is limited.

## Real-world applications

- Sensor readings
- Counters
- Banking/database fields
- Embedded devices
- Image and audio data

## Key points / exam notes

- Range depends on bit width.
- Unsigned maximum is 2^n−1.
- Signed two's-complement range is asymmetric around zero.

# 1\. 24 Overflow and Underflow Concepts

## What is it?

Overflow occurs when a mathematical result is outside the upper end of the representable range. Underflow occurs when a result falls below the lower representable limit; in floating-point arithmetic, underflow can also refer to values becoming too small to represent normally.

## How does it work?

With fixed-width integers, arithmetic is performed using a fixed number of bits. If the mathematical result requires more range than those bits provide, the representation cannot store the true result. The exact observed behavior depends on the number format and programming language.

## Formula / Rule

Unsigned n-bit maximum = 2^n−1. Overflow occurs when result > maximum. Signed overflow occurs when the true result is outside the signed range.

## Step-by-step example: 4-bit unsigned overflow

1\. 4-bit unsigned range is 0–15.  
2\. Take 15: 1111₂.  
3\. Add 1: 1111₂ + 0001₂ = 10000₂.  
4\. The result needs 5 bits, but only 4 are available.  
5\. Therefore, the operation exceeds the 4-bit range and overflow occurs.

### Overflow and underflow comparison

| **Feature**     | **Overflow**                   | **Underflow**                                          |
| --------------- | ------------------------------ | ------------------------------------------------------ |
| Basic idea      | Result is too large            | Result is too small                                    |
| Integer example | 15 + 1 in 4-bit unsigned       | Below the minimum representable value                  |
| Typical concern | Fixed-width integer arithmetic | Very small floating-point values and lower-bound cases |

## Where is it used in computers / programming?

- Important in integer arithmetic, data types, counters and embedded software.
- Floating-point underflow matters in scientific and numerical programs.
- Overflow can cause incorrect results, security bugs or unexpected program behavior if not handled.

## Real-world applications

- Digital counters
- Timers
- Financial and scientific software
- Embedded systems
- Signal processing

## Key points / exam notes

- Overflow means above the representable maximum.
- Underflow means below the representable minimum or too small for the floating-point format.
- Always check the data type and bit width before judging whether overflow occurs.

**Digital Circuit Connection: Binary Addition**

Number systems do not have one single circuit diagram. However, binary numbers are processed by digital logic circuits. A Half Adder is a simple and important example because it shows how the binary rule 1 + 1 = 10 is implemented in hardware.

## Half Adder

A Half Adder adds two one-bit binary inputs, A and B. It produces two outputs: Sum and Carry.

SUM = A XOR B  
CARRY = A AND B

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABXgAAAK8CAIAAADat0BMAAAACXBIWXMAAB7CAAAewgFu0HU+AABnvklEQVR4nO3deXxU1cE//puEPQiEgGFxt6CoIApWcUVci4JilVoWUXCppVbFBbVWXPogat31EUEFBJW6C1qoSC3gjhVBBMSFfd/CTkJIfn/M65vfPJOFSXKTTML7/YevmXPPPffcGyfhfubcc5Ly8vICAAAAgDAkV3YHAAAAgOpD0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhKZGZXcAACBRLFmyZPLkyV999dW8efOWLVuWmZm5a9euunXrNmrUqEWLFu3bt+/QocMFF1zQsmXLyu5pWe07ZwpAJcgDoGx+/PHHQn/BnnHGGXvd97rrrit034kTJ8bfgT59+hTze/6nn36qmHOJv7X4zZ8/vxTHjUdYF62Yc0xOTq5du3b9+vXT09MPP/zwjh07du3adeDAgY8//vinn366a9euEnU4EQ4Up0J/anE2W6tWrcaNGx900EGnn376NddcM3LkyNWrV5eo/6WTk5MzduzYE088MZ5OJiUlnXjiiaNGjcrOzo7zNIv6BFX8ZQnrTEtxsvl69+5d6I4ff/xxqY/SoUOHeM6oRJ5++unSXWQAjGgAqNq2bdv2zjvvFFNh7Nix9957b0V1p2qomIuWm5ublZWVlZW1bdu2DRs2xGytV6/exRdffO21155xxhlV5UAVIDs7e+PGjRs3bly6dOn06dNHjhyZnJx84YUXPvjgg0cddVQ5HXTGjBl/+MMf5s2bF2f9vLy8L7/88ssvv7znnntmzpyZkZFRTh3LF9ZlSfwzBaB6MEcDQNX21ltvbd++vZgKY8eOrbDOVBWJcNF27Njx6quvdu7cuUuXLj/88EM1OFA5yc3NnTBhQvv27cePH18e7T/wwAOdO3eO/9472rJly7Zu3Rp6l+JRistSRc8UgKpI0ABQte31lviXX3759NNPK6YzVUVCXbSPP/64ffv2o0ePrjYHKg+7d+/u3bv3jBkzwm32uuuuu+eee3Jzc8NttsLEf1mq+pkCULUIGgCqsOXLl3/88cd7rfbyyy9XQGeqigS8aLt27brqqqsefPDBanOg8pCbm3v99deH2ODdd989YsSIEBusFPFclupxpgBUIYIGgCps3Lhx8XxF+frrr2dlZVVAf6qEhL1od91118iRI6vTgUL3/fffz549O5SmPvzww6FDhxZT4fzzz3/++efnzZu3YcOGrKyslStXzpo167nnnvvd735Xr169UPoQluIvS3U6UwCqCkEDQBUW51QCmZmZEydOLO/OxC/+NSyOPPLI0I9eMRct/xxzc3M3bdr0yy+/TJw48Y477jj44IOL2euGG24o6Y10xR8o3J9adLPZ2dkrV66cMGHC6aefXlT9eEaj7FVWVtYf//jHvLy8Qrf+6le/+uSTTyZNmnTttde2adOmcePGtWrVat68efv27f/whz+MHz9++fLlDz/8cJMmTcrek6KEdVkS/0zD8vXXXxfz/2S/fv0K3WvKlCnF7PWnP/2pgs8CoNoQNABUVf/9738LndftgAMOKFjo6YmIir9oSUlJjRo1OvTQQyNrBPz8889jx45t1KhRoZUjt4UJfqDyU7NmzebNm3fr1m3q1KlFrb+4atWqsh9ozJgxP//8c6GbjjvuuM8+++yUU04pZve0tLTbbrvthx9+uPrqq5OTy/2fUmW5LFXrTAGoNvzNAKiqCr0NbtGixX333VewfPLkyevWrSv/TiW6Sr9oKSkpffr0mTVr1iGHHFJohc8++2zy5MlV6EDloUaNGkV9BR3K2gfPPvtsoeUNGzZ8++23mzZtGk8jjRs3Hjly5GGHHVb2/sSpFJelip4pAFWdoAGgSsrJySl0WbtLL730kksuqVmzZkz57t27y2l1wCokcS7aIYccMmHChKIegH/uueeq3IFC16xZs0LLixqjEb+FCxfOmTOn0E333HNPUblMgijRZanSZwpAlSZoAKiSJk+evHbt2oLll112WaNGjc4+++yCmzw9kVAXrW3btkUtFvCvf/1r27ZtVe5A4Vq5cmWh5W3bti1jy1OnTi20vH79+ldffXUZGy9vJbosVfpMAajSBA0AVVJRjwBEnri+7LLLCm79+uuv58+fX+49S2CJdtEGDRqUlJRUsDwrK+urr76qigcKS05OzpgxYwqW165d+9xzzy1j419//XWh5Z07d27QoEEZGy9XJb0sVfdMAajqBA0A5WXatGlJe/P888+XouXNmzcXuiDCpZdeGrmfvPjiiws+CBDEveBCeYvnyiQlJY0bNy7EgybgRWvRokWbNm0K3fTtt98m2oEq4KeWk5OzevXqiRMnnnXWWTNnzixY4brrrktPTy91+xE//fRToeXFT4tYiUp9WarcmQJQbQgaAKqe119/fdeuXQXLe/bsGXmRlpZW6IMA48aNK2qhu2ovMS/ar3/960LLlyxZUkUPVFLR+UVkeYXu3btPnz69YM2OHTv+z//8T9mPuHr16kLLi18QtIKFclmqxJkCUC0JGgCqnkIfAWjZsuXJJ5+c/7bQBwGWLVv28ccfl2PPElhiXrSipv3ftGlTFT1QOenRo8eUKVPq169f9qZ27NhRaHlaWlrZG69gxV+W6nSmAFQtggaAKmbRokWffvppwfL8RwAiEvzpiQqWsBetqEfls7KyquiBwpWSkvKb3/zmww8/fPvtt8u+3kTxCp3GIjGV8bJUoTMFoIoSNABUMWPHji10JH/Mt/FFPQjw1ltvFfU9ZzWWsBdt8+bNhZbXqVOnih4oXElJSfXq1cvIyAixzaIW+9y4cWOIRylXcV6WanCmAFRRggaAKqbQyfZiHgGIKPRBgK1bt77zzjvl0rMElrAXbd26dYWWhz64vcIOFK6cnJy33nqrU6dOIV7/ou7Ply5dGtYhylucl6UanCkAVZSgAaC8nHHGGXl7c91115Wozc8///zHH38sWB7zCEBEwj49Ec+VycvL69OnTyiHS+SL9uWXXxZaHvp0fWU/UAX/1KLt2LHj8ssv/+KLL0Jp7Ve/+lWh5YU+XJPI9npZyvtMixoOk5OTU/yOu3fvLlGDAFQ5ggaAqqTQGQ2DqKUToqWlpZ111lkFyz/66KNVq1aF3LMElrAXbdmyZQsWLCh0U/v27avigUohP7/YuHHjzJkzr7nmmho1ahSslp2dfcUVV4Qyo0THjh0LLf/Pf/6zdevWsrcfilAuS3mfaVHTQ2zbtq34HYuq0Lhx4zJ2CYAEIWgAqDKys7Nff/31QjedcsopSYWZPHlywcp79ux55ZVXyrmziSKRL9rf//73Qstr165d1GqUCX6gskhLS+vYseOIESPeeOON5ORC/n3y448/PvXUU2U/UKFBUhAEW7duffHFF8vefrjKclnK+0zr169f6PCfva6Zunjx4kLLE/xBHgDiJ2gAqDLef//9sGZxq/SnJypMwl60WbNmjRgxotBN5513XmpqapU7UFguvvjiQYMGFbrpoYce2uu35Xt1xBFHtG3bttBN9913X8LOX1CKy1IBZ3rooYcWLMzMzPz555+L2mXLli2FPsrUoEGD9PT0sncJgEQgaACoMop6BKAU5syZM3v27LBaS2SJedF++umniy66aNeuXYVuvf7660M5SkUeKFxDhgxp2rRpwfINGzYMHz687O0PHDiw0PLMzMzf/va3GzZsiKeRjRs3Xnvttb/88kvZ+xOnUlyW8j7TgtOpRrz22mtFtfb6668XOkfDSSedVOiQDQCqIr/QAaqGDRs2/POf/wyxwRDvwBNWAl60nJyc0aNHd+jQYdmyZYVW6NSp03nnnVfGo1TkgcpD/fr1b7311kI3PfbYY2WfqeHKK6887LDDCt309ddfn3zyycVPPJmZmfnoo48eeeSRI0eOzM3NLWNn4leKy1LeZ3raaacVuuMjjzwyd+7cguVLliy55557Ct3l1FNPLaYnAFQtggaAqmH8+PFFTdVeOq+++uqePXtCbDABJcJFy8vL27x586JFi95///077rjjsMMOu+qqq7Zs2VJo5dq1az/33HMF18JIqANVjOuvv77QuQZXrVo1atSoMjZeu3btZ599tqjTX7hwYadOnbp27frCCy8sWLAgMzNz9+7da9asmTNnzsiRI/v06XPAAQfceuutRa0YWq5KelnK+0wvvfTSBg0aFCzfsmXLqaee+re//e3777/fuXPnrl27fvzxxyeeeOLXv/51oZOq1qhRo1+/fkUdBYCqJ56lqgAoRqHPGwdlW95y4sSJMTXLY9K+SZMmxXku8RswYEAoVyYUFXDRyn7Foj3//PNFnUsVOlD0/wN7bbaY/xn+8pe/FLrLoYcempOTE9f/AcW64447ynimQRD8+OOPZTnNirks5XGm+YoaZFEiffr0Kep8Q/k1UlSKMWXKlPgbASB+RjQAVAE//PDDV199VbD8wAMP3LNnz15/148ePbrQ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Y489NgiC3/3udzVr1iymJkB18txzz7Vo0SK65KWXXpowYUL+22uvvXbdunXRFa6++upu3brFtPP888//7//+b0zhYYcd9uKLLy5dujQrK2vNmjVvvfVWwecI/vOf/9x444177WdqampkBOCePXvWrFnz4osvNmzYMKZO8fP7FmP69Ol9+vQpGJGcdNJJI0aM+P777zMzM7Ozs9etWzd79uxRo0YNGDCgSZMme222pFMOL1iwoOCIx1WrVsXslZ6eXujYyPHjxxd1oPyrV5Rjjjlmr6cDAFQ9ZXrwghIqOBfDww8/nL/1oosuit7UokWLnJycSuxtBf5vCCSocv0lM2nSpJjD7b///mvXrs3Ly3vppZdiNh166KFbt26NaWHTpk0x0z0EQdC5c+ft27fH1MzNzR04cGBMzaSkpFmzZsU0GFOn4K1ywakoGzduXIrT3717d+vWrWOaqlu37ssvv1zMXjk5Oe+9997pp5++bdu2oup8+OGHMc3GTDlcp06dTZs2Fd+9+IOGfPFcPSpF9A+lsvsCwD7BiIYKFfMlUnJycq9evfLf9unTJ3rrypUrC/5jEaDaOP/88//whz9El0Qel1iyZEnMYxTJycljxoypX79+TAtPPvlkzBo96enpb7zxRr169WJqJiUlPfXUUx07dowuzMvLu//++0va7QsvvDCmZNOmTSV6cCNi5MiRCxcujCkcN25czJN0MVJSUrp37z5t2rTU1NSi6owaNSr6bfPmzV944YXokl27dr322msl7TAAQJwEDRWn4FjWLl26tGzZMv9tt27dYr6ai/nHIkA18/e///1Xv/pVdMm777572mmnbdmyJbrw1ltvjflOPuLNN9+MKbnhhhuKerggOTl5yJAhMYX//Oc/Y+bN2au0tLSYkpSUlOTkEv89HTduXEzJJZdccskll5S0nRimHAYAKp2goeJMmTJl+fLl0SUxX1vVrl37sssuiy6ZMGFCKVYLA6gqUlNTx44dm5KSEl24bNmy6Ldt27Z94IEHCu67du3auXPnxhReeumlxRzu/PPPjxkWkZWV9cknn5Sozxs2bIgpadWqVYlaCIJg06ZNX375ZUxhwYc7SsGUwwBApRM0VJyCXx/169cv6f8aOXJkdIWsrCyjW4Hq7aSTTrrjjjuK2lqrVq1x48bVqlWr4KZ58+bFlNSrV69NmzbFHKtGjRrt2rXbazvFmzhxYkxJwYcp9mru3Lkxa0zWqlWr4IyVpZBQUw5v3749qWgxD8gAANWGoKGCbN68OWYsa5wqcXRrZU8gQnXjf7CqouJ/2wwZMuS4444rdNMDDzxQMBqIWL9+fUxJRkbGXh9hiFnqotB2CpWXl7d27dqXXnrp5ptvji5PS0u75ZZb4mkh2tq1a2NKMjIy6tSpE1M4bNiwou7SmzVrVrDZhQsXfv7559El+QMZGjdu3LVr1+hN48aNiwk7AABCIWioIOPHj9+1a1cpdpw5c2ZJv20DqFpq1qxZcN3KIAiSkpIuvvjiovbavHlzTEkx8yMWU6dgO9Hyv5NPTk7OyMgYMGBAdP20tLT33nsvIyNjr8eNETOHZRAEDRo0KGkjBZlyGABIBIKGClKWgQmm7AKqt+++++6hhx4qWJ6Xl3fllVcW9a17w4YNY0q2b9++12MVrFOwnXjUq1fv6quv/u677wqdpXKvCq7KuXXr1lK0E82UwwBAghA0VIQffvjhiy++iC65/fbbixm3fOqpp0ZXHjt2rNGtQHWVnZ3dt2/frKysQrd+/vnnhWYQQRAUXF1izZo1e11mcuXKlXttJx55eXlZWVkxsx7Eb//9948pWb16dVEXIU4JOOVwampqMX/snnjiifI7NABQiQQNFaHgV0bFzxwWs3X16tWTJ08Ov1sACWDIkCGzZ88upsK999777bffFiwvOO/jjh07il9JIScnZ86cOTGFRx11VFwd/b927tw5duzY448/PubePk5HH310zFob2dnZMZF0EAR33HFH/m15hw4dim/TlMMAQIIQNJS73NzcmMXSGzduXPzU4hdccEFMiacngGrps88+e/jhh6NLGjRoEDO34u7duwsd8pCRkXHMMcfEFL755pvFHG7y5Mnbtm2LLqldu3bMILIYke/kc3NzV69ePWbMmAMOOCB664oVKy6++OJSDDpr3Ljxr3/965jC559/vqTt5KuKUw4D7AtmzJhxww03dOrUqVmzZnXr1q1Zs2aDBg0OPvjgTp069e7d+29/+9v777+/bt26gjtmZmbGhMUxKzRHq1OnTkzlmL93BVuLKD7F3rlzZ3p6esG9Yv4aQiFCmaKcYkyaNCnmmvfq1Wuvex188MHRu9SuXXvDhg0V0FsoP375VBUV9mPatm3b4YcfHvM/xqhRo3Jzc7t06RJTfuuttxZs4d57742plp6evn79+kIPt2fPnhNOOCGmfo8ePaLrFHyOIGbw/88//1xweoUnn3yyFKf/7LPPxrSTnJw8efLkourH/FswIyMjeuvw4cOD0vr+++8LHm7VqlUx1dLT04s/o71ePSpL9A+lsvsC+5D58+fHv25xwV/FJfqlWrt27ZjKW7duLb61fJ999llRzb7wwguF7tKyZcsyXhyqPSMayl3BL4viWXE9ZhEyo1uB6mfQoEE///xzdMlFF1105ZVXJiUljR49OmaOxscee2z69OkxLdx4440xt/0bNmy47LLLdu7cGVMzLy/vxhtvnDlzZnRhUlLSPffcU6I+H3bYYQXnjBgyZMjGjRtL1E4QBNdcc01MzpKbm9uzZ88PPvigpE0FphwGSDBz58499dRTP/vsszjr73WOofLzzDPPlGIT7EVlJx3AvsIvn6qiYn5MBW+nmzZtumbNmvwKMQsoBEFwyCGHbNmyJaadQr/JP/zww1966aVly5ZlZ2evXbv2nXfeOeWUUwpWu/7662Nai+fro5ycnILTOtxyyy2luAhTp04tdDrJ3/zmN6+++uqiRYt27Nixa9eulStXTpgwIWacavSIhgULFsS0UKIph5s1a5aTkxNTx4iG6iT6h1LZfYF9wp49e9q3b1/w13sxvvvuu5hGKmxEQ61atVavXl2wzRkzZhS1ixEN7JURDQBUtA0bNlx99dUxhSNGjIhei6FPnz49e/aMrrB48eKbbropZq/rrrvuj3/8Y0zhzz//3L9//wMPPLBWrVr7779/jx49Pv3005g6nTt3fvLJJ0vR+ZSUlAcffDCm8JlnnlmyZElJm+rSpcuLL76YlJQUUz5p0qRevXodeuih9erVq1OnTosWLbp3717MrJMJO+Xw9u3bC30kON/dd99dHscFqFwfffRRzDTGxx577BtvvLFixYrdu3dv27Zt0aJFb7/99qBBg2Iel64U2dnZI0aMKFj+9NNPV3xnqDYEDQBUtOuvvz7mC/N+/fpdfPHFMdWee+65Fi1aRJe89NJLEyZMiKn2zDPP3H///cnJJfiLdsUVV3zwwQelXpyye/fup512WnRJVlZW6e6Z+/btO2nSpIKrXcbPlMMAiWbKlCnRbxs2bPif//zn0ksvbdGiRY0aNVJTUw855JAePXo8+uijixcvnjZtWrdu3Ur0Vyx0zz//fE5OTnTJypUr33777crqD9WAoAGACvXKK6+88cYb0SUHHXTQU089VbBm48aNX3rppZjCa665JmZ27qSkpL/+9a/Tp08/++yz93r0Y4899vXXXx8zZky9evVK3vf/X8GZGl555ZVCl+Hcq/POO2/OnDmDBg1q0KBBPPVbtmx52223/ec//4m8/fDDD1esWBFd4fzzz49ZOzPGMcccE/Md2sSJE0sxzQQAhVq2bFn02yOOOKLgRML5Tj/99AkTJpRureWyaN68ef7rFStWvPPOO9Fbhw8fnh89JCcnZ2RkVGjnqPoEDQBUnOXLl//pT3+KLolM/VjUPfZ5550X82TE2rVrr7322oI1TznllClTpsyZM+fhhx++8MILW7VqlZ6eXqNGjYYNGx522GFnnnnmX//612nTpn377beXXXZZ2U+kU6dOl1xySXRJXl7e7bffXrrWMjIyHn300WXLlo0fP37gwIEdO3Y88MAD69evn5KS0rBhwwMPPPCUU07p37//U089NXfu3OXLlz/88MNHHnlkZF9TDgMkmphlj+fPn19w4ptKd+aZZ7Zu3Tr/bfS8jzEPU1xwwQXWs6SkkvIKzNAGUB5iHkT3yydhRf+k/JigGvChhgp2yy23PPbYY9ElBx988E033XTBBRe0atUqzkYyMzPT0tKiS1JTU7dt21Zo5Tp16mRlZUWXbN26tX79+sW01rt37xNOOCF68qM5c+a0bds2CIJx48b17ds3v/xf//rXXXfd9d///je/pGXLlsXMHASBEQ0AAAAhOv/882NKlixZcvPNN7du3bpJkybnnHPOHXfcMWHChEp/Zu2qq66KDiPyBzVEj25o3br1OeecU9E9o+qrUdkdAACgghRc5QT2TeU6uuecc8457bTTCl0ecsOGDR999NFHH30UBEGNGjXOPPPMP//5z/E88lYeGjRo0Ldv3+eeey7y9pVXXnnooYd++umnL7/8Mr/On/70J783KAUjGgAAAML0+uuvH3vsscXXycnJmTJlSrdu3bp27ZqZmVkh/YoVPXHS9u3bR40aFb2qZf369fv161cZ/aLKEzQAAACEqVmzZp9//vkDDzzQpEmTvVaeNGlSz549K6BXBR111FFdunTJf/vEE0/84x//yH/br1+/OFdEghiCBgAAgJDVrVv37rvvXrFixYQJE/785z8fd9xx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ixTu2bPniiuu2LlzZxAETz311EEHHRS9y9y5c/Pn4Bw2bNjNN99c6MiUtLS0f/7zn5H7+by8vMhR4nfTTTdFXvz44495pX08pCg1a9a87LLLIq/L79EMAKgsggYAqptdu3YFQZCSklK5jyS0adOmY8eOQRFPT4wdOzYIgu7duzdq1KiCO1Y6eXl5Y8aMCYIgLS3tggsuCIKgb9++QRDs3LnzH//4R1lavv32248//vggCN5///3IZRk6dOhXX30VBMFFF11UcBaDp556KvLiuOOOu+2224ppuXbt2i+99FLk9eeffz5z5sz4exV58iUIgj179pR6+Yl4NGvWrPwaB4BKIWgAoLo58MADgyDYs2fPhx9+WLk9idwkT5s2bcmSJdHln332WWR+gSo0F+DUqVOXLl0aBEHPnj0jDzv07t07suJDwekVSqRGjRqjR4+uWbNmEAQ33njjP//5zwceeCAIgqZNm44YMaJg/SlTpkRe/PnPf97rLBvHHXfcGWecEbNjPCInGwRBkyZNIqtjhCgnJyd/nEuHDh3CbRwAKp2gAYDqpnv37pEX/fr1e+655zZu3FhZPfn9739fs2bNvLy8cePGRZdHhgbsv//+5513XqkbP+aYY5JKrtSjPPLThMhAhiAIWrRocdZZZwVB8MUXX8yfP7/UJxIEQdu2be++++4gCDZt2nThhRfu3r07CILhw4fvv//+MTVXrVq1ePHiyOs4r965554befHpp5/G36XHH3888uLEE0+Mf6/i5ebmrl+/ftKkSWeffXZkkoszzzyzU6dOYbUPAAlC0ABAdXPXXXe1bNkyCIKNGzf+8Y9/bNq0adu2ba+88spnnnnm66+/zsnJqbCepKenR54yiH56Iisr6/XXXw+CoHfv3jVq1KiwzpTF5s2b33nnnSAIDjvssFNOOSW/PD90GD16dBkPceeddx577LFBEORPA3HJJZcUrLZ8+fLIi6ZNmzZv3jyeliPNBkGwYsWKvVbesmXL9OnTL7300kgYFARB8U9nFG/NmjXRKU9KSkrTpk27du06bdq0pKSk7t27R64qAFQzggYAqpuMjIwZM2bk3w/n5ubOnTt3zJgxN9xwwwknnNCkSZOrr7564cKFFdOZK664IgiChQsXfvHFF5GS9957LzMzM39Tqc2dO7cUs0Bv27atFMd67bXXIlMz9unTJ7r8kksuSU1NDYJg7Nixe/bsKcvp1KxZ8+abb85/+5e//KXQavnjUxo3bhxny/k1Cx3bEpMFNGzY8IwzznjrrbciW5944on8Jy9ClJSUdNNNN40YMSKy4AgAVDOCBgCqoUMPPfSTTz756KOPrrjiipjvvTdv3vziiy8effTR+WPjy9UFF1yQnp4eRA1qiHxV3q5du/wFDhNf/nMTMUFDampqZNzBqlWrJk2aVJZDbN26NXqVkKKChgrTqVOnmTNn3njjjeXReF5e3uOPP37QQQeVcXoLAEhMggYAqq2zzjprzJgxK1euXLRo0dtvv33XXXedcsopkekDc3JyBg0alD88vvzUqlXr8ssvD4LgH//4R3Z29po1ayJTVJZxOENFmjdvXmQNiJNOOqlVq1YxW/NPpIz3zIMGDVq0aFEQBJFZId9666033nijYLXihycUqhSDIIIgmDlzZokmjyxURkZGwREls2fPvvfee1NTU7Ozs/v371/ohJcAUKUJGgCo/g455JAePXr8z//8zyeffDJ//vzIqpNBEAwePDh6yob8xQUijwkUY/v27TG7FCOytMTGjRvff//9V155JScnJyUlpXfv3qU4kUpRcBrIaF26dInMiDFx4sT169eX7hD//Oc/X3jhhSAIWrduPXXq1MjUFQMHDizYYORYQRCsW7du1apV8TQ+e/bsmH2jRWcB27Ztmzt37uDBg2vVqpWTk3PXXXeNHDmydGdUlNTU1Hbt2g0ZMuSDDz6IZF533HHHjh07wj0KAFQuQQMA+5Yjjjji/fffr1evXhAEa9asmTlzZv6m/Afm16xZU3wja9eujbxo1KjRXo94wgkntGnTJgiCl19+OTKG4txzz23WrFlpeh+lYladyMnJyV8yY+DAgQUbTElJiUyyuHv37ldeeaUUJ7Jx48arr746CIKUlJQxY8acdtppkfkX161bd8MNN8RUbtGixcEHHxx5HefypfnVoqexLFRqaurRRx89bNiwN998M5IC3HzzzfnrXIbrjDPOiARemzZtmjZtWnkcAgAqi6ABgH1ORkZGu3btIq+XLFmSX55/B/vtt98Ws/uePXvmzJkTeX3IIYfEc8TI8wUTJ06M7BgZ41AlTJo0afXq1XFWLt3TE9dff31kbMLgwYNPOumkIAiGDBly1FFHBUEwfvz4d999N6b+OeecE3nx1FNPRZaoKMa3336bfxufv+NedevW7Q9/+EMQBNu3b7/33nvj3KukDjjggMiLX375pZwOAQCVQtAAwL5o06ZNkRd169bNLzz66KP322+/IAhWrFgxY8aMovadNGlSZNmIjIyMOIOGPn36JCcn5+bmBkHQsGHDiy66qPRd/38qZtWJEmUHs2fPnjVrVonaHz9+fGSxz2OPPXbIkCGRwtq1a7/00kspKSlBEFx//fUx0zHkD3P45ptvHnvssWIaz87OHjBgQOT1iSeeeMIJJ8Tfsfvvv79BgwZBELz88ssLFiyIf8f4LVu2LPIiMi0FAFQbggYA9jmjRo364YcfIq+PPPLI/PKUlJTIGgpBENxwww2RNCHGunXrBg0aFHnds2fPOI94wAEHdOnSJfL6sssui2dmh0Swfv36999/P/J64cKFxeQX1157baRaiYKJVatWDRw4MAiCWrVqvfzyy7Vq1crfdOKJJ0au8+rVq2+66abovdq1a3fppZdGXt9+++1PPfVUoY1v3rz5wgsv/Oabb4IgSEpKuv/+++PvWBAETZo0iRx3z549+QlIiP7zn//897//jbwuOMUmAFRtpfgyBAjFvvZh3NfOl0p05JFHdu/e/W9/+9vkyZNnz569fPnyHTt2ZGdnr1y58oMPPvj9738fefw+CILjjz8+Zt/Zs2dHZiIMguCwww4bPnz4zz//vGvXrp07dy5cuPDpp5/OH+5et27dn376KWb3/IESxx57bPwdjswNkZqaWsYTD13+CqCdO3cuvmb+PXN6enpWVlac7Xft2jWy14MPPlhw686dO4844ohIhffffz9608aNG/OfcwmCoFOnTmPGjFm8ePGuXbs2b948a9asv/3tb02aNMmvMGjQoJjG839SBReGyJeZmZmWlhYEQVJS0uzZs+M8qeIb3759+5w5c+67777U1NRInebNm+/evTv+xgEg8fm3PlSafe3Ge187XypR/pyOxatXr95XX31VcPe///3v8ew+cuTIgvtWs6AhfyaLV199da+VO3ToEKn8xhtvxNP4888/H6nfqVOnnJycQut8+umnycnJQRC0bNkyMzMzetPChQsPP/zweH5S11xzTcE7+XiChry8vL/97W+Rat27d4/npGIa36ukpKS33nor/pYBoErw6AQA+6Ijjzxy6tSphT60f8stt4wYMaKY1RkaNmz46quvRhZKqMa++eabyNSV6enp+U+UFKNET08sWrTolltuCYKgXr16Y8aMiUzHUNDJJ5984403BkGwYsWK/CdWIlq1avX5559fccUVkSSiUPvvv//w4cNHjBiRP0qlpG688cbIyIgJEyZEL1ASirS0tFdffTWeawsAVUtS3t6mawbKSf7g7Yhq/2Hc186XShRZtHLmzJn//e9/ly9fvmHDhg0bNuTk5DRo0OCggw5q3779RRdddMEFFxR/87lhw4YXX3zxo48+mjdv3oYNG4IgSE9Pb9u27TnnnDNgwICiBk3kD7Y/9thji1+6IlqjRo02b96cmppa0pkay9UNN9zwzDPPBEFw8803Fz/nYsS2bdtatGixdevWlJSUpUuXtmjRoqiaubm5Z5555vTp04MgeOaZZyLTNBRl586d7dq1++mnn4IgmDx58nnnnRdTYf78+a+//vqUKVMWL168fv362rVrN23atH379l27du3Zs2dRgVH+TyojI6P4ZTUeeeSR22+/PQiCc88991//+lcxNQs2XlDdunXT09OPOeaY888/v0+fPunp6fE0CABVi6ABKs2+duO9r50vAADsmzw6AQAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAIRG0AAAAACERtAAAAAAhEbQAAAAAISmRmV3AIBqJSkpqbK7ANVZXl5eZXcBAPZC0ABAWQkXoMJEf9yEDgAkJkEDAKUnYoBKFPkAihsASDSCBgBKQ8QACULcAECiETQAUDLFRwzudqBcFfUBFDcAkDgEDQCUQFE3OW5voGLkf9YK/TAmJSX5MAJQ6QQNAMSr4I2NWxqoLEUlDrIGACpdcmV3AICqQcoAiangJ9EUKgBULkEDAHsXc9+Sl5cnZYDEUfAjKWsAoBIJGgDYi4IpQ2X1BCiGrAGABCFoAKA4UgaoQmQNACQCQQMARZIyQJUjawCg0gkaAIiLlAGqCp9WACqXoAGAwvkiFKoHn2UAKpigAYC98wUpVC0+swBUIkEDAIWI/grUHQtURdGfXIMaAKhIggYAAAAgNIIGAGL58hOqH59rACqMoAGA4nhuAqoun18AKoWgAQAAAAiNoAEAAAAIjaABgP/DehNQnVh7AoCKJ2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQlOjsjsA7KOSkpIquwsAAED4jGgAAAAAQiNoAAAAAEIjaAAqSF5eXl5eXmX3AgAAKF+CBgAAACA0ggagQuWR8Cr7/5HKMXLkyKTCLFiwoPgdMzMzC+514IEH7tq1q9D6v/rVr6JrHnnkkfE0mJycXLt27fr16zdv3vyoo446++yzr7vuuhEjRvz888/hnH+UrKysiRMn3nHHHZ07d27VqlV6enqNGjVSU1MzMjKOP/74nj17Dh06dMaMGdnZ2XE2GP+1PfLIIwutGafLL7880k6h17B4c+fODfMiAsC+zaoTABCMHj26qPJhw4aVtLXly5c/9dRTt99+e1m79f/k5eVlZ2dnZ2dv37599erV8+fPnzp1amTTKaeccvfdd59//vllP8rmzZsff/zx4cOHr1mzJmbTjh07duzYsXbt2lmzZr3xxhtBEKSlpV122WXPPvtsjRp7+bdEuNcWAEh8RjQAsK/78ccfP/vss0I3jR07ds+ePaVoc9iwYZs2bSpbv+Ly6aef/uY3v+nVq9f27dvL0s706dPbtWt33333FUwZCrVp06YRI0YUNXAjX3lcWwAgwQkaANjXFfWVexAEK1eunDJlSina3LRpU0V+Xf/aa6916dJlx44dpdv9zTffPPPMM5cuXRpur4LyubYAQIITNACwT8vNzR07dmwxFYq5VS7e008/vXz58tLtGy01NTUyfcauXbtWrlz5r3/9a9CgQQ0aNIip9tVXX/Xp0yc3N7ek7U+fPr3QHU866aQRI0Z8//33mZmZ2dnZ69atmz179qhRowYMGNCkSZN4Wi7ptV2wYEHBSUNWrVoVs1d6enqh04uMHz++qAPlX8OiHHPMMfGcEQAQD0EDAPu0qVOnLlu2LLrktNNOi3773nvvZWZmlqLlnTt33nvvvWXoWqzatWs3b9783HPPffTRRxctWtS1a9eYCu+88864ceNK1GZOTs4111yTlZUVXVi3bt2XX375888/v+aaa4466qiGDRvWrFmzSZMm7dq1u/LKK1944YXVq1e/9957p59+elJSUjGNl9+1BQASmaABgH3aqFGjot82b978hRdeiC7ZtWvXa6+9VrrGR48ePX/+/NJ3rmiNGzd+9913Y+7bgyAYMmTI7t27429n5MiRCxcujCkcN25c3759i9krJSWle/fu06ZNS01NLaZauV5bACBhCRoA2Hdt2bLl3XffjS7p1atX69atO3XqFF1Yoqcnoles3LNnz5133lmmLhatZs2azz//fMyYgsWLF0+fPj3+RgqOgLjkkksuueSSsnevPK4tAFAlCBoA2HeNHz9+586d0SWRb/Jjvs//6quv4h+Y0KFDh9/+9rf5b997773PP/+8zD0tXJs2bTp37hxT+K9//SvO3Tdt2vTll1/GFA4cOLDsHQvK59oCAFWCoAGAfVfM1+lt27Y99thjgyD43e9+V7NmzWJqFm/o0KE1atTIfzt48OCydLJ4p59+ekzJt99+G+e+c+fOjVlgslatWieffHIoHSuna1s627dvTyraTTfdVN4dAIB9iqABgH3UwoULY8Ya5H/Z3rhx45ipFseNGxdzT16M1q1b9+/fP//tjBkz3n///bJ1tkgHHXRQTMn69evj3Hft2rUxJRkZGXXq1IkpHDZsWFG36M2aNSu05fK7tgBA4hM0ALCPivkiPTk5uVevXvlv+/TpE7115cqVH374YfyN33vvvfXq1ct/e+edd5Zi4cl4FFznMv51HArWLNha6ZTrtQUAEpygAYB9UW5u7tixY6NLunTp0rJly/y33bp1a9SoUXSFmDUUite8efPoAflz5859+eWXS9fV4m3evDmmJKbbxShYc+vWrWXuUblfWwAgwQkaANgXTZkyZfny5dElMZMU1q5d+7LLLosumTBhwqZNm+I/xO23356enp7/dsiQIVlZWaXqbHEWL14cU9K0adM4991///1jSlavXl32TlbAtS2p1NTUvKI98cQT5XdoANgHCRoA2BcVnICwX79+MRMQjBw5MrpCVlbWa6+9Fv8hGjZseNddd+W/Xbp06TPPPFOGLhfuP//5T0xJ+/bt49z36KOPTklJiS7Jzs7+4osvYqrdcccd+ffkHTp02GuzFXBtAYBEJmgAYJ+zefPmd999txQ7lnR9hIEDB0ZP1jh06NBt27aV4rhFmTNnzieffBJTeO6558a5e+PGjX/961/HFD7//PNl6VKFXVuARLN169Z//OMfN9xww4knnnjIIYc0aNCgZs2ajRs3Puqooy699NLHHnts3rx5e21k5MiRhU6+u2DBguJ3zMzMLGZ5nZo1a6alpbVq1eqiiy566KGHFi1aVE5Nbdy4sVmzZjG7/PGPfyzmcE8++WRM/dq1a8+dO3ev14qEVsxIQqBc+TCSmPaF/y2HDx9e6r+b33//fXRTBQf89+7dO7pC8ffPRxxxREzfCjZY1LD/rKysk046KabyIYcckp2dHf+lePbZZ2NaSE5Onjx5clH1Y0Y0ZGRklN+1jVi1alVMtfT09OJPKv5ruI+IvhSV3ReontasWXPLLbfEM5/uCSec8MUXXxTTVFFrDA8ePLj4PpToAbSUlJTrr79+586d5dHUO++8E1MnKSlp+vTphR5r0aJFqampMfX/9re/7e2Sk+iMaABgn1OWL89Lum/fvn3btm1b6sMVZf369RdeeGHBxxzuu+++mjVrxt/ONddcc/jhh0eX5Obm9uzZ84MPPihdxyry2gIkgg8//LBdu3aPPvroli1b9lp55syZMav/Rvvxxx8/++yzQjeNHTs2xJWA9+zZ89xzz/Xo0SOvwFdfZW/q4osvjl5pKAiCvLy8q6++eteuXQV3v+6667Zv3x5d0qFDh8GDB5exV1Q6QQMA+5Yffvgh5v789ttvLyaSP/XUU6Mrl/SfesnJyUOHDg2l59nZ2atXr54yZcqgQYMOP/zwKVOmxFS4+OKLY1aO3KuaNWuOGDEiJpvYsmXLhRde2LVr19dee23x4sU7d+7MyspatWrVxIkT16xZU0xrFXxtASrduHHjzj///OJ/N8avmLx15cqVBX/tl9HkyZNfffXV8mjq6aefbtasWXSFhQsX3nvvvTF7jRo1KmZ541q1ao0ePbpGjRqh9IpKJGgAYN9ScCXFCy+8sJj6MVtXr149efLkEh3xwgsvPP3000u0S7Tt27fnP7PavHnzc8899/HHHy/4vdmvf/3rV155JTm5xH/Zu3Tp8uKLLyYlJcWUT5o0qVevXoceemi9evXq1KnTokWL7t27xywnEaPir22c8q9hUe6+++7yOC5QvX388cf9+/cvOCjg4osvfvvtt1esWJGVlbV58+aFCxe++uqrV155ZcFnBKIVXBs4RkmHfeU/NbZnz541a9a8+OKLDRs2jKlT/BFL3VTjxo0LPkn36KOPzpo1K/9t5HmTmDpDhgw55phj4ukSiS6M5y+A0vBhJDFV7/8t9+zZ07Jly+hzbNy4cU5OTjG7fPfddzGf1ksvvTR/617naIgoaqBsPHM0xKNXr17btm0ry5WZPHlywdUu9yp6jobQr21EKHM07NVf/vKXUl+6xBd9ppXdF6g+srOzYx49C4Jgv/32++CDD4raZcuWLffee++LL75Y6NaY7/aDIDjttNOi39apU2fTpk1FNR7P9DRjxoyJqdO4cePya6p3794xdY477rjdu3dHtv72t7+N2dqxY8f8rVR1RjQAsA/58MMPV6xYEV1y/vnnxyzxGOOYY445+OCDo0smTpy4cePGEh33pJNOuvjii0u0S5xOPfXUf/3rX6+88krxX5Tt1XnnnTdnzpxBgwbFM5lZEAQtW7a87bbbohfXrKxrC1ApRo4c+fPPP0eXJCUljR8/vmvXrkXtst9++w0ZMqR///6Fbo0ZFNa8efMXXnghumTXrl1lXAm44CizTZs25ebmllNTTz31VMwDFLNmzXrkkUeCIHjnnXfeeuut6E0emqhmBA0A7EMKjjstfmx/RMy/GrOyskrxT70HH3yw+LvuYkSWE0tNTW3WrFmbNm3OPvvs6667bsSIEb/88suMGTPiX8+yeBkZGY8++uiyZcvGjx8/cODAjh07HnjggfXr109JSWnYsOGBBx54yimn9O/f/6mnnpo7d+7y5csffvjhI488Mn/3Sry2ABVv3LhxMSWXXnppMSlD8bZs2RKzNnCvXr1at27dqVOn6MIyTpqblpYWU5KSklKKZ+7ibKpx48YFl0y+//77v/zyy4EDB8aU33vvvUcffXQpekJiSsor80SjQOnEPBHtw0iCiP4/0/+WUA34UEPoNm3a1LRp05j5a6dOndqlS5fSNThixIjrrrsuuuTbb7899thjn3vuuT/+8Y/R5fPmzWvTpk3BFjIzM2Nu/lNTU7dt2xZdsn79+qZNm0aXtGnTZt68eeXXVBAEffv2jQllatWqlZ2dHV3SsWPHL774otRxPAnIiAYAAIASmDt3bkzKUKtWrZNPPrnUDcYMVWjbtu2xxx4bBMHvfve7mIWByjKoYeLEiTEl8Qw9K2NTTz31VPPmzaNLYlKG2rVrjx49WspQzXgGpoIUzAWjRQbENm7c+Fe/+tXxxx9/wQUXxKz4BQBQdgWXF4F9UxlH96xduzampFmzZnXq1CldawsXLoyZM7hv376RF40bN+7atet7772Xv2ncuHFDhw4t0W15Xl7eunXr3n///UGDBkWXp6WlFVz3IfSm0tLSnn/++e7duxfVpocmqiUjGhLC7t27MzMzf/nllw8//HDYsGGnnXbaSSedNH/+/MruFwAAECszMzOmZL/99it1azGDFJKTk3v16pX/tk+fPtFbV65cWXB9ikLlr+ybnJyckZExYMCAzZs3529NS0t77733MjIyKqCpbt265UcnMU444YTbbrstnj5QtQgaEtSXX355yimnLF68uLI7AgAA/B+NGjWKKdm6dWvpmsrNzR07dmx0SZcuXaJXC+7WrVvM4WLWpyipevXqXX311d99913M8pnl2tSTTz4Z8wBF4KGJak3QkLg2bdo0ePDgyu4FAADwf+y///4xJatXr961a1cpmpoyZcry5cujS2K+/K9du/Zll10WXTJhwoRNmzaV4lgReXl5WVlZMVM/lHdTaWlpMU9bBEFw+eWXH3XUUWXvBglI0FBpUlNT8/6fnTt3fv311507d46pM3HixKysrMroHQAAULijjz465nv47Ozszz77rBRNFZzcsV+/fkn/18iRI6MrlHEl4J07d44dO/b444+PCTjKu6mCc1iUelYLEp+gISHUqVOnQ4cOb7/9dkwcuHPnzpUrV1ZWrwCAaiYPyMvLK/M6r40bN/71r38dUzh8+PCStrN58+Z33323FB2IZ+2JyPeaubm5q1evHjNmzAEHHBC9dcWKFRdffHHM2hkV0BT7CEFDAklLS4t+HCsiNze3UjoDAAAUJWaOxiAI3nzzzX/+858lamT8+PGle+Bi5syZ8+bNi6dmUlJSRkbGFVdcMW3atJi5Hv773/8+++yz8R80xKao9gQNCSQzM3PFihXRJbVq1TrooIMqqz8AAEChrrnmmsMPPzy6JC8v7/LLL580aVJRu2zduvX+++9/6aWX8kviGZhQlJLue9hhhz300EMxhUOGDNm4cWNJDx1iU1RXgoaEkJWVNWvWrEsvvXT37t3R5b179w5lmhYAACBENWvWHDFiRMy/1bdu3dq1a9cePXq8++67K1eu3L1799atW3/66afx48dfddVVLVq0GDJkyJYtWyKVf/jhhy+++CJ699tvv72Yxz1OPfXU6Mpjx44t6dMKAwYMiJl8MTMzc+jQoSVqJPSmqJYEDZUmfzXapKSkOnXqHH/88VOnTo2u0KZNm4cffriyugcAABSjS5cuL774YlJSUkz5u+++26NHj5YtW9aqVatBgwatWrX6/e9/P3r06G3btkVXK7hK5YUXXljM4WK2rl69evLkySXqcEpKyoMPPhhT+MwzzyxZsqRE7YTbFNWSoCFBDRgw4PPPP2/SpEkl9iGJcuaCk5gq5RcOAFRFffv2nTRpUsHVLvcqNzd33Lhx0SWNGzc++eSTi9nlggsuiCkpxZMX3bt3P+2006JLsrKy7r777pK2E25TVD+ChgT16quv3n333aWbGwYAAKgY55133pw5cwYNGtSgQYO9Vu7YsWOnTp2CIPjwww9jZmc7//zzY5bMjHHMMcccfPDB0SUTJ04sxbQIBadXeOWVV7799tuSthNuU1QzgoYEtXPnzmeeeaZbt25ZWVmV3RcAAKBIGRkZjz766LJly8aPHz9w4MCOHTseeOCB9evXT0lJadiw4RFHHHHRRRc99NBD33333cyZM0888cSgsMEIxT83EdG1a9fot1lZWa+99lpJe9upU6dLLrkkuiQvL+/2228vaTvhNkU1k1T2VWSJR2ZmZlpaWnRJampq/mNaOTk5K1as+PDDD+++++61a9dGVxs6dOidd95ZcR2NYgQ14G8EVAPRf9B9qAGoAIKGClJ80JDv3//+91lnnRVdcthhh/3888/l3r/CCBoAfyOgGhA0AFDBBA0VJM6gIS8vb7/99tu+fXt04caNG2P2BSg/7kmgmvGhBqCCmaMhsUTWyI0p3Lp1a6V0BgAAAEpK0JBYpk6dumPHjpjCyl3kEgAAAOInaEgIe/bsWbp06YgRI3r37h2z6aijjqpXr16l9AoAAABKqkZld2DftX379nhmWxwwYEAFdAYAAABCYURDQuvcufOf//znyu4FAAAAxEvQkKBq1qx5ww03TJo0qUYNo04AAACoMtzEJoqaNWvWr1+/efPmbdq0Of3003/729+2bNmysjsFAAAAJZNkOWUAokVPH+NvBFQDPtQAVDCPTgAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQA8H/k5eXlv05KSqrEngBlF/0pjv50A0D5ETQAAAAAoRE0AAAAAKERNABQHE9PQNXl8wtApRA0ABDLg9xQ/fhcA1BhBA0AAABAaAQNABTC2hNQ1VlvAoDKImgAYO9kDVC1+MwCUIkEDQAUzlegUD34LANQwQQNAMTFF6RQVfi0AlC5BA0AFCnmi1B3L5D4Yj6nhjMAUPEEDQAUR9YAVYiUAYBEIGgAYC9kDVAlSBkASBBJ/ggBEI+C+YK/IJAgfDwBSChGNAAQl4L3LYY2QCKQMgCQaIxoAKAEigoX/DWBCubDCEDCEjQAUDLFD2TwZwXKlQ8gAIlP0ABAaXhuAhKKf9EBkDgEDQCUnrgBKp1/ywGQaAQNAJSVuAEqhX/FAZCYBA0AhEnoAOXKv9wASHyCBgAAACA0yZXdAQAAAKD6EDQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNAAAAAChETQAAAAAoRE0AAAAAKERNABQZaxbt+6555679NJLjzjiiPT09Jo1azZp0qRdu3b9+/d/4403srKy9trCgAEDkpKSkpKSkpOTFy1aVEzNzMzMpAKSk5MbNGhw+OGH//a3vx07dmwxRyzF7uedd16k2iOPPFL8WcyfP79OnTpJSUmNGjVavnz5Xs+6EsV/wcuv5eifRXJy8rfffltUzdGjR0eq3XvvvcU0kq9OnTr7779/q1atzjnnnMGDB7/99tvx/E+4105GS0lJadiw4THHHNO/f/+PP/64dI0DQEXLA4CEt2PHjsGDB6emphbzF61x48YPP/zwrl27impk27Zt++23X379e+65p5gjbtq0aa9/Q1u3bj1nzpywdl+6dGmDBg2CIKhTp868efOK6lhOTs6JJ54YaeHFF1+M4+JVmhJd8PJrOeZn0bVr16Jqjho1KlJnyJAhxTdSlMaNG99yyy1btmwp6RnF2X6PHj127NhR0sYBoIIZ0QBAoluxYsXpp5/+0EMPbd++vZhqGzduvP322ydOnFhUhTfffHPr1q35b8eMGZOXl1eWji1cuPDcc89dv359KLsfeOCBjz32WBAEu3btuvLKK/fs2VPoXo8++uiXX34ZBEHXrl379+9fukNXjNAveCgt//Of/5wxY0Yo3Sho48aNjz76aLt27SI/o9C98847/fr1K4+WASBEggYAEtq2bdvOPffcr7/+OvL28MMPf/jhh2fOnLlu3brdu3dv3Lhx3rx5L7/8cp8+ferWrVt8U5Hvq2vVqhW5VVuyZMm///3vvXYgIyMjP57Pzc3dvHnz9OnTe/bsGdm6evXq4p90KNHuAwYM+M1vfhMEwVdffVVosz/88MOQIUOCIGjUqNGIESP22vnKVboLXn4t16tXL/LirrvuKvWho3+ge/bsyczMXLRo0YQJE2677bZmzZpF6ixevLhr164LFy4sY/t5eXk5OTlr1659//33Tz311EiFN954Y86cOaXuPwBUhPIeMgEAZXHFFVdE/mAlJSXdd999OTk5RdXMzMwcPHjwxIkTC936888/JyUlBUFw8cUXz5o1K9Jm7969i2otfyh7zI1fvvzRBEceeWSIuy9fvrxRo0ZBENSuXfv777+P3rRnz55OnTpF9op8h5/ISnrBy6/l/J/FscceG8lxgiD44IMPCtaM59GJon6geXl52dnZf/3rX1NSUiI1jzvuuPhPaq/tZ2dnt2/fPlLn8ccfj79lAKh4RjQAkLjmz58/duzYyOthw4bdc889+XdxBTVs2HDYsGEXXnhhoVtHjx6dl5cXBEHfvn3bt2/ftm3bIAjefvvtzZs3l65vN910U+TFjz/+mFfyJwKK2r1ly5ZPPPFEEARZWVn9+vWLfoDi0Ucf/fzzz4Mg6NatW37+krBCv+ChtDx06NBISHHXXXeV4qdWvJo1a95///2PP/545O2sWbMmTJgQYuOXXXZZ5HWpn9YBgIohaAAgcT355JORu8ETTjjhtttuK3U7eXl5Y8aMCYIgLS3tggsuCIKgb9++QRDs3LnzH//4R+naPOCAAyIv9uzZU4q1BorZvV+/ft26dQuC4Ouvv37ooYcihT/88MM999wTBEHjxo0T/6GJ8rjgobTcvn37yHMrs2fPLmNPinLDDTecfvrpkdcvvfRSeRwi/xkNAEhMggYAEteHH34YeXHjjTdGvogunalTpy5dujQIgp49e9auXTsIgt69eycnJwf/72n/Uog0GARBkyZN6tSpE+7uzz//fOPGjYMguO++++bOnZubm3vVVVft2rUrCIKnn3468e8zy+OCh9XyAw88UKNGjSAI/vrXv+bk5JSlM0XJH64yY8aMsMZN5OTkvPnmm5HXHTp0CKVNACgnggYAEtSqVasWLVoUeX322WeXpan8W9DIt99BELRo0eKss84KguCLL76YP39+KdrMHyGfv9hkiLs3b978qaeeCoIgOzu7X79+jzzySOShiR49evTq1asUhzvmmGOSSq5+/fqlOFZQPhc8rJZbtWp11VVXBUHw008/ldOIg86dO0dysY0bN/7yyy9laSo3N3f9+vWTJk06++yzIxNSnHnmmflTdQBAYhI0AJCgVqxYEXmx//77Z2RklLqdzZs3v/POO0EQHHbYYaecckp+ef6d6ujRo+NvbcuWLdOnT7/00ksjA/iDICjRMx3x7967d+8ePXoEQfDNN9/ccccdQRA0adJk+PDh8R+rsoR7wcuj5SFDhkRGkdx///2RcSLhSktLyx91sm7duhLtu2bNmuisJyUlpWnTpl27dp02bVpSUlL37t0jVwAAEpmgAYAEtWHDhsiLtLS0srTz2muv7dy5MwiCPn36RJdfcsklqampQRCMHTs2es7FGDE3fg0bNjzjjDPeeuutyNYnnnjijDPOKOboZdl9+PDhTZo0yX/77LPP7r///ns/4cLMnTu3FFNGb9u2rRTHKuMFr4CWW7ZsOXDgwCAIVqxY8cwzz5SiJ3sVefIliPrfuIySkpJuuummESNGNGzYMJQGAaD8CBoASHRlmZ0hiBpsH3N3mpqaeskllwRBsGrVqkmTJpW02U6dOs2cOfPGG28sXa/i2X3//fe/7777Iq/PPPPMyCyGia+cLni4Ld95550NGjQIgmDYsGFbtmwpRWeKlz81Qxn/741u8PHHHz/ooIPKOMkFAFQAQQMACSo9PT3yYuPGjaVuZN68eV999VUQBCeddFKrVq1ituYvElmKm7eZM2dOmTKl1B2Lc/f8IQylHstQwcrvgofbcnp6+i233BIEwYYNG/7+97+XtDN7tWnTpsiL/KENccrIyCg4rmT27Nn33ntvampqdnZ2//79E3/ZEQD2cYIGABJUixYtIi/Wrl27Zs2a0jVScO7AaF26dGnZsmUQBBMnTly/fn2hLUTf+G3btm3u3LmDBw+uVatWTk7OXXfdNXLkyOI7UMbdq5yyX/AKa3nQoEFNmzYNguDxxx8v6UwKxdu4cePq1asjryOHKIvU1NR27doNGTLkgw8+iIyPuOOOO3bs2FHWXgJAuRE0AJCgWrRoceihh0Zef/TRR6VoIScnZ9y4cZHXAwcOLLiqQkpKSmTKyd27d7/yyit7bTA1NfXoo48eNmzYm2++Gbnlu/nmm/MXqizv3cuiYladCP2Cl2vL9evXv+uuu4Ig2LZt2//8z/+U6EyL9/HHH0cenUhPTz/ssMPCavaMM87o2LFjEASbNm2aNm1aWM0CQOgEDQAkrnPPPTfy4sknnyzF7pMmTcr/YnmvSjSYv1u3bn/4wx+CINi+ffu9995b0o6VcfeEVX4XvJxavv766w866KAgCIYPHx5i4pP/v+vpp58e1hwNEQcccEDkRRlXzQSAciVoACBx/fnPf47cp82cOfPRRx8t6e4lupWdPXv2rFmz4q9///33R2YTfPnllxcsWFDSvpVx95KqmFUnyu+Cl1PLtWvXHjJkSBAEWVlZYSU+Tz/99IwZMyKvBwwYEEqb+ZYtWxZ5UbNmzXBbBoAQCRoASFxHHXVU7969I69vv/32oUOH5ubmFlV58+bNd9555/vvvx95u379+vzXCxcuLOZ2+tprr41UK9HdbJMmTW666aYgCPbs2RO5WS2RMu6egMrvgpfrj7Jfv35HHnlkEEbis3v37nvvvffmm2+OvO3QocMFF1xQlgZj/Oc///nvf/8beV1wOkwASByCBgAS2v/+7/9G7gNzc3P/8pe/tGnT5tFHH/3mm282btyYk5OTmZm5YMGCcePG9e3bt0WLFsOGDdu1a1dkx3Hjxu3evTsIgs6dOxd/V3bddddFXrz66qvZ2dnx923QoEFpaWlBELzxxhtz5swp6amVcfdEU34XvFx/lCkpKQ888EAQBHv27HnmmWfi2SVfXl7eli1blixZ8v777w8ePPjggw++77779uzZEwRBenr6+PHjS9RaUXbs2PHdd9/df//9F154YWTqh+bNm5922mmhNA4A5UHQAEBC22+//T788MPjjjsu8nbhwoW33nprhw4d0tPTa9asmZaW1qZNm759+44bNy5mHv7877Tzv+UuyvHHH9+hQ4cgCDZs2DBhwoT4+9awYcPIEol5eXl//etf498xlN0TTfld8PL+Uf72t7+N7LV9+/a9Vl6zZk3+DJTJyckNGzY85JBDunXr9vDDD69atSpS59BDD500adKvfvWrODtQVPsR+atORLqXlJT0zDPP1KhRoxSNA0DFEDQAkOgOPPDATz755NZbb61Xr14x1dLT0x9++OFu3boFQfDNN99Exgikp6dfcsklez1E6Z6eCILgxhtvbNKkSRAEEyZMmDlzZon2LfvuiaP8LngF/CiTkpKGDh0aZ+XiNW7c+NZbb509e/YJJ5wQSoMx0tLSXn311XiuAwBUIkEDAFVAvXr1HnnkkUWLFj3zzDM9evRo1apVo0aNatSo0bhx43bt2vXv3//NN99csWLFbbfdVrt27SDqJvOKK66IlBSvV69e++23XxAE//rXv1auXBl/x+rXr3/77bdHXt99990lPa8y7p44yu+CV8yP8txzz+3cuXOclfPVqlUrsoDlWWedddttt7399tsrV6585JFHIh0IS926dQ844IDzzz//iSee+PHHHy+//PIQGweA8pAUedgPAAAAoOyMaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABCI2gAAAAAQiNoAAAAAEIjaAAAAABC8/8BczorYJYwSuYAAAAASUVORK5CYII=)

| **A** | **B** | **SUM** | **CARRY** |
| ----- | ----- | ------- | --------- |
| 0     | 0     | 0       | 0         |
| 0     | 1     | 1       | 0         |
| 1     | 0     | 1       | 0         |
| 1     | 1     | 0       | 1         |

## Why is this circuit relevant?

The circuit is not a 'number system circuit'. It is a hardware circuit that operates on binary values. Larger adders are built from similar logic and are used inside the Arithmetic Logic Unit (ALU) of processors.

# Truth Tables: When Are They Applicable?

A truth table is not required for decimal, binary, octal or hexadecimal notation itself. Truth tables become applicable when number systems are connected to Boolean logic and digital circuits.

| **Concept**           | **Truth table applicable?**         | **Reason**                                                   |
| --------------------- | ----------------------------------- | ------------------------------------------------------------ |
| Decimal number system | No                                  | It is a numerical representation system.                     |
| Binary number system  | Not by itself                       | Binary uses 0/1, but a truth table describes logic behavior. |
| Logic gates           | Yes                                 | Truth tables describe outputs for every input combination.   |
| Half Adder            | Yes                                 | It is a digital logic circuit.                               |
| ALU operations        | Yes, for individual logic functions | Boolean operations can be described with truth tables.       |

# Binary Addition Rules

| **A** | **B** | **Sum** | **Carry** |
| ----- | ----- | ------- | --------- |
| 0     | 0     | 0       | 0         |
| 0     | 1     | 1       | 0         |
| 1     | 0     | 1       | 0         |
| 1     | 1     | 0       | 1         |

The last row is the important hardware case: 1 + 1 produces a Sum of 0 and a Carry of 1, which together represent 10₂.

# Master Conversion Tables

## Binary ↔ Octal

| **Binary** | **Octal** | **Binary** | **Octal** |
| ---------- | --------- | ---------- | --------- |
| 000        | 0         | 100        | 4         |
| 001        | 1         | 101        | 5         |
| 010        | 2         | 110        | 6         |
| 011        | 3         | 111        | 7         |

## Binary ↔ Hexadecimal

| **Binary** | **Hex** | **Binary** | **Hex** |
| ---------- | ------- | ---------- | ------- |
| 0000       | 0       | 1000       | 8       |
| 0001       | 1       | 1001       | 9       |
| 0010       | 2       | 1010       | A       |
| 0011       | 3       | 1011       | B       |
| 0100       | 4       | 1100       | C       |
| 0101       | 5       | 1101       | D       |
| 0110       | 6       | 1110       | E       |
| 0111       | 7       | 1111       | F       |

## Common Decimal / Binary / Octal / Hex Values

| **Decimal** | **Binary** | **Octal** | **Hexadecimal** |
| ----------- | ---------- | --------- | --------------- |
| 0           | 0          | 0         | 0               |
| 1           | 1          | 1         | 1               |
| 2           | 10         | 2         | 2               |
| 3           | 11         | 3         | 3               |
| 4           | 100        | 4         | 4               |
| 5           | 101        | 5         | 5               |
| 6           | 110        | 6         | 6               |
| 7           | 111        | 7         | 7               |
| 8           | 1000       | 10        | 8               |
| 9           | 1001       | 11        | 9               |
| 10          | 1010       | 12        | A               |
| 11          | 1011       | 13        | B               |
| 12          | 1100       | 14        | C               |
| 13          | 1101       | 15        | D               |
| 14          | 1110       | 16        | E               |
| 15          | 1111       | 17        | F               |
| 16          | 10000      | 20        | 10              |

**One-Page Revision Sheet**

| **Item**             | **Remember**                                              |
| -------------------- | --------------------------------------------------------- |
| Decimal              | Base 10; digits 0–9                                       |
| Binary               | Base 2; digits 0–1                                        |
| Octal                | Base 8; digits 0–7                                        |
| Hexadecimal          | Base 16; digits 0–9, A–F                                  |
| MSB                  | Most significant / normally leftmost bit                  |
| LSB                  | Least significant / normally rightmost bit                |
| Decimal → Binary     | Repeated division by 2                                    |
| Binary → Decimal     | Use powers of 2                                           |
| Decimal → Octal      | Repeated division by 8                                    |
| Octal → Decimal      | Use powers of 8                                           |
| Decimal → Hex        | Repeated division by 16                                   |
| Hex → Decimal        | Use powers of 16                                          |
| Binary → Octal       | Group 3 bits                                              |
| Octal → Binary       | Each digit → 3 bits                                       |
| Binary → Hex         | Group 4 bits                                              |
| Hex → Binary         | Each digit → 4 bits                                       |
| Unsigned n-bit range | 0 to 2^n−1                                                |
| Signed n-bit range   | −2^(n−1) to 2^(n−1)−1                                     |
| Overflow             | Result above representable maximum                        |
| Underflow            | Result below representable minimum / too small for format |
| Nibble               | 4 bits                                                    |
| Byte                 | 8 bits                                                    |