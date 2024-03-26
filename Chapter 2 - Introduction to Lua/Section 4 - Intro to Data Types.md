In [Section 2.3](./Section%203%20-%20Variables.md), we learned about variables. So far, we've stored one type of value, which was always enclosed by quotation marks. However, Lua offers several different types of values, each with unique characteristics.

In most programming languages, a **data type** is the type of value a variable can hold. However, Lua handles things a bit differently. Lua is a **dynamically typed language**, meaning variables themselves don't have types; only values do.

Each data type in Lua has its own set of functions and use cases. In this chapter, we'll introduce three data types: strings, numbers, and nil.

# Strings

A **string** is a data type that represents a sequence of characters. So far, we've already been working with strings extensively in this guidebook:

```lua
print("Hello World!") -- "Hello World!" is a string!
```

For a string to be valid, it needs to be enclosed by matching quotation marks. There are three ways to create strings in Lua:

```lua
local string1 = "I am a string in double quotation marks!"
local string2 = 'I am a string in single quotation marks!'
local string3 = [[ I am a string in double brackets. ]]
```

Strings created using double brackets have a unique property: they can span multiple lines, similar to multi-line comments.

```lua
local longString = [[
  I am extending

  For multiple lines!

  Sweet.
]]
```

Apart from the ability to span multiple lines, strings behave the same regardless of how you create them.

> ✨ **Use Double Quotation Marks**
> <br>
> Most modders stick with using double quotation marks for strings, so it's a good practice to follow.

In modding, strings are used for a lot of things, such as:

- Assigning a name to an enemy.
- Assigning a name to a player.

# Numbers

A **number** is.... well, a number.

Here are examples of numbers in Lua:

```lua
local number1 = 5 -- A whole number.
local number2 = -10 -- A negative number.
local number3 = 8.99 -- A decimal number.
local number4 = -9.8 -- A negative decimal number.
```

If you've used a calculator, you know that very large (or small) numbers are often represented in a less precise way. The same applies to Lua. Consider the following:

```lua
local myNumber = 10205128392138213934321194
print(myNumber)
```

Instead of printing the exact number you typed, the output will be "1.0205128392138e+25". In Lua, large numbers are represented in scientific notation.

If a number becomes too large even for scientific notation, Lua represents it as infinity:

```lua
local myVeryLargeNumber = 99999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999999

print(myVeryLargeNumber) -- Prints "inf"
```

Similarly, if you add too many decimals to a number, it will lose precision.

In modding, numbers are used for various purposes, such as:

- Specifying the health of enemies.
- Specifying the amount of coins a player has.

# nil

**nil** is a data type that indicates the absence of a value. Recall the following snippet from [Section 2.3](./Section%203%20-%20Variables.md):

```lua
local coolVariable
print(coolVariable) -- Prints "nil"
```

Because we didn't assign a value to the variable, attempting to print its value resulted in "nil".

You can also explicitly assign `nil` to a variable:

```lua
local coolVariable = nil
print(coolVariable) -- Prints "nil".
```

There's no difference between explicitly assigning `nil` and not assigning any value at all. Both represent the absence of a value. Choosing which approach to use is a matter of personal preference.

# Quiz

1.) Write a code snippet which does the following:
  - Initializes a variable named "foo" with a value of `5`.
  - Print out the value of the variable.
  
<details>
<summary>Solution</summary>

```lua
local foo = 5
print(foo)
```
</details>
<br>

2.) Let's say you wish to assign a description to an item. Out of all of the data types covered so far, which data type would be used for assigning the description?
  
<details>
<summary>Solution</summary>

string

</details>
<br>
