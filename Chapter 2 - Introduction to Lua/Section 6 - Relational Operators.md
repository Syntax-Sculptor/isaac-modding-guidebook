# Booleans

A **boolean** is a data type that can only hold two values: `true` and `false`. Just like the other data types we've seen, you can assign them to variables.

```lua
local boolean1 = true
local boolean2 = false
```

>⚠️ **Booleans are case-sensitive!**

# Relational Operators

A **relational operator** compares two operands and returns a boolean value based on the result. Here's a list of Lua's relational operators:

| Operator | Description | Example | Result
| --- | ----------- | ----------- | --- |
| == | **Equal To:** Checks if two operands are equal | 5 == 5 | true |
| ~= | **Not Equal To:** Checks if two operands are not equal | 8 ~= 8 | false |
| > | **Greater Than:** Checks if the left operand is greater than the right operand | 10 > 3  | true |
| < | **Less Than:** Checks if the left operand is less than the right operand | 10 < 3 | false |
| >= | **Greater Than or Equal To:** Checks if the left operand is greater than or equal to the right operand | 5 >= 5 | true |
| <= | **Less Than or Equal To:** Checks if the left operand is less than or equal to the right operand | 15 <= 8 | false |

>⚠️ **Relational Operators aren't Assignment Operators!**
><br>
>Many beginners confuse the assignment operator (`=`) with the equal to operator (`==`). Remember, the assignment operator assigns a value to a variable, while the equal to operator checks if two values are equal.

Using a relational operator is similar to using arithmetic operators. Here's an example:

```lua
local myValue = 90
print(myValue > 100)
```

Running this will print out "false". We assign `myValue` the value 90, then we print out whether it's greater than 100. Since 90 is not greater than 100, the expression evaluates to `false`.

Here's another example:

```lua
local myValue = 40 >= 35
print(myValue)
```

Running this will print out "true". We assign the result `40 >= 35` to the variable. Since 40 is greater than 35, the expression evaluates to `true`, and that is stored in `myValue`.

You can also compare strings.

```lua
local fruit1 = "Apples"
local fruit2 = "Bananas"
print(fruit1 == fruit2)
```

Running this will print out "false" because the values of `fruit1` and `fruit2` are not equal.

# Relational Operators with Two Different Types

When comparing two operands with different data types, you can use the equal to operator (`==`) or the not equal to operator (`~=`). For example:

```lua
print(5 == "5")
```

Running this will print out "false" because the two operands have different data types (number and string), so their values cannot be equal.

However, you **cannot** use other relational operators to compare operands with different data types. For example:

```lua
print(5 <= "5")
```

This code will cause an error because you cannot compare a number with a string using the less than or equal to operator.

# Relational Operators with Strings

We've went over that you can use `==` and `~=` to compare strings. But what happens if you use other relational operators?

In Lua, when you compare two strings using other relational operators, they are compared in alphabetical order. For example:

```lua
local string1 = "red"
local string2 = "blue"
print(string1 > string2)
```

Running this will print "true" as "red" comes alphabetically after "blue".

String comparisons are case-sensitive. If two characters have the same letter but different cases, the lowercase letter is considered alphabetically greater. For example:

```lua
local string1 = "Red"
local string2 = "red"
print(string1 > string2)
```

Running this will print out "false" because the lowercase "r" in `string2` is considered alphabetically greater than the uppercase "R" in `string1`.

# Quiz

Do not run these code snippets.

1.) What does this print?

```lua
print(true == false)
```

<details>
  <summary>Solution</summary>
  false
</details>
<br>

2.) What does this print?

```lua
local myVariable = 2 + 5
print(myVariable <= 7)
```

<details>
  <summary>Solution</summary>
  true
</details>
<br>

3.) What does this print?

```lua
local myCurrentValue = 10

print(myCurrentValue + 5 > 20)
```

<details>
  <summary>Solution</summary>
  false
</details>
<br>

4.) What does this print?

```lua
local variable1 = 5
local variable2 = variable1 >= 5
print(variable2)
```

<details>
  <summary>Solution</summary>
  true
</details>
<br>
