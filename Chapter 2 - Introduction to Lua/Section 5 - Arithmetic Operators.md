In [Section 2.4](./Section%204%20-%20Intro%20to%20Data%20Types.md), we introduced numbers as one of the fundamental data types in Lua. It was also stated that each data type has their own unique functionality. When it comes to numbers, we can use **arithmetic operators** to perform mathematical operations. 

Here is an example of an arithmetic operator in action.

```lua
print(2 + 7)
```

Running this will print out "7".  The `+` symbol is the addition operator, and it adds the two numbers together.

You can also use arithmetic operators with variables:

```lua
local myNumber = 10 
print(myNumber + 15)
```

Running this will print out "25". We first declare `myNumber` with a value of 10, and then we add 15 to its current value before printing the result.

Here is another example:

```lua
local number1 = 10 -- Declare a variable named "number1" with a value of 10.
local number2 = 30 + number1 -- Declare a variable named "number2" with the value of `number1` added to 30.
print(number2) -- Prints 40
```

# List of Arithmetic Operators

Lua 5.3 offers eight arithmetic operators:

| Operator | Description | Example | Result
| --- | ----------- | ----------- | --- |
| + | **Addition:** Adds two operands | 10 + 4 | 14 |
| - | **Subtraction:** Subtracts two operands | 10 - 4 | 6 |
| * | **Multiplication:** Multiplies two operands | 10 * 4  | 40 |
| / | **Division:** Divides two operands | 10 / 4 | 2.5 |
| // | **Floored Division:** Divides two operands and rounds down the quotient | 10 // 4 | 2 |
| ^ | **Exponent:** Raises the left operand to the power of the right operand | 10 ^ 4 | 10000 |
| % | **Modulo:** Divides two operands and returns the remainder | 10 % 4 | 2 |
| - (unary) | **Unary minus:** Inverts the sign of the operand | -(10 - 4) | -6 |

<br>

>⚠️ **Division by Zero**
> <br>
> Dividing by zero is undefined in mathematics and can lead to unexpected behavior in programming. In Lua, dividing by zero will not throw an error but will instead return `inf` (infinity).

# Operator Precedence

When using multiple arithmetic operators in an expression, the order in which they are evaluated is determined by **operator precedence**, also known as the **order of operations**. This is similar to the PEMDAS rule you might be familiar with from mathematics.

```lua
local finalAnswer = 5 - 1 + 3
print(finalAnswer)
```

Running this will print out "7". The operations are performed in this order: 

1. `5 - 1` is evaluated first, resulting in `4`.
2. Then, `4 + 3` is evaluated, resulting in the final answer of `7`.
   
However, operator precedence can change the order of evaluation:

```lua
local finalAnswer = 2 + 5 * 10
print(finalAnswer)
```

You might expect this code to print "70", but it actually prints "52". This is because multiplication has higher precedence than addition.

Below is the order precedence for arithmetic operators in Lua:

1. **Parenthesis** (expressions inside parenthesis are evaluated first, following the same precedence rules)
2. **Unary minus**
3. **Exponent**
4. **Multiplication and Division** (evaluated from left to right)
5. **Addition and Subtraction** (evaluated from left to right)

Here is an example of this in action.

```lua
local myAnswer = (10 * 2) / 5 + 1
print(myAnswer)
```

Running this will print out "5". The operations are performed in this order:

1. First, the expression inside the parenthesis, `10 * 2`, is evaluated first, resulting in `20`.
2. Then, `20 / 5` is evaluated (division has a higher precedence than addition), resulting in `4`.
3. Finally, `4 + 1` is evaluated, resulting in the final answer of `5`.

Congratulations! You've learned how to utilize arithmetic operators. Just like variables, this is one of the most important things to know when modding (And coding in general).

# Quiz

Do not run these code snippets.

1.) What does this print?

```lua
print(10/5)
```

<details>
  <summary>Solution</summary>
  2
</details>
<br>

2.) What does this print?

```lua
local myVariable = 2 + 5
print(myVariable)
```

<details>
  <summary>Solution</summary>
  7
</details>
<br>

3.) What does this print?

```lua
local myCurrentValue = 10
myCurrentValue = myCurrentValue ^ 2
print(myCurrentValue)
```

<details>
  <summary>Solution</summary>
  100
</details>
<br>

4.) What does this print?

```lua
local variable1 = 10
local variable2 = variable1 + 5
print(variable2)
```

<details>
  <summary>Solution</summary>
  15
</details>
<br>

5.) What does this print?

```lua
local variable1 = 10
local variable2 = variable1 - 2
local variable3 = variable2 * 2
print(variable3)
```

<details>
  <summary>Solution</summary>
  16.
</details>
<br>

6.) What does this print?

```lua
local myVariable = 2
print(myvariable / 2)
```

<details>
  <summary>Solution</summary>
  The code errors as it tries to perform an arithmetic on a nil value as there is no variable named `myvariable`
</details>
<br>

7.) What does this print?

```lua
print((8 + 2)/2)
```

<details>
  <summary>Solution</summary>
  5
</details>