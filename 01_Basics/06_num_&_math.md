# Number and Math in JavaScript ->
JavaScript provides built-in Number and Math objects for handling numerical values and performing mathematical operations.


## Number Object :- 
The **Number** object is used to work with numbers in JavaScript and provides methods to manipulate them.

**Examples and Methods :**
- ![alt text](../Images/image-44.png)

- **Examples:**
- ![alt text](../Images/image-45.png)



## Math Object :- 
The **Math** object provides properties and methods for mathematical constants and functions. It is a static object, so you can use its methods directly without creating an instance.

**Common Math Methods:**
![alt text](../Images/image-46.png)



### Generating Random Numbers:
- **Random decimal number between 0 and 1:**
- ![alt text](../Images/image-47.png)

- **Random number between 1 and 10:**
- ![alt text](../Images/image-48.png)

- **Random number between `min` and `max`:**
- ![alt text](../Images/image-49.png)


- ### Examples:
- ![alt text](../Images/image-50.png)



## Key Notes 
1. ### Number Object:
- Use `.toString()` to convert numbers to strings.
- Use `.toFixed()` and `.toPrecision()` to format numbers.
- Use `.toLocaleString()` for locale-specific formatting.

2. ### Math Object:
- Provides essential mathematical operations like rounding, finding minimum/maximum, and generating random numbers.
- `Math.random()` is great for randomness but often combined with `Math.floor()` to get integers.

3. ### Random Numbers:
To generate random numbers in a range, calculate using the formula:
`Math.floor(Math.random() * (max - min + 1)) + min`.
Understanding these tools is essential for working with numbers and performing mathematical operations in JavaScript!