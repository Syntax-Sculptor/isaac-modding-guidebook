# Introduction to Conditional Statements

While modding, you'll often encounter situations where you want to execute code only if a certain condition is met. For example, you might want an item to work in specific rooms or an enemy to move only when the player is moving. This is where conditional statements come in.

A **conditional statement** evaluates a condition and executes a block of code if the condition is evaluated as `true`. In [Chapter 2.6](./Section%206%20-%20Relational%20Operators.md), we looked at relational operators, which play a key role in working with conditional statements.

The basic structure of a conditional statement in Lua looks like this:

```lua
if condition then
    -- Code to run if the condition is `true`
end
```

If `condition` evaluates to `true`, the code between `then` and `end` will be executed. `then` marks the beginning of the code block to be run, and `end` marks the end of the conditional statement.

Here is an example of a conditional statement in action:

```lua
if 5 <= 10 then
    print("The number is less than or equal to 10.")
end

print("End of conditional.")
```

Running this will print out:

```
The number is less than or equal to 10.
End of conditional.
```

IF we change the condition to `15 <= 10`, the output will be different:

```lua
if 15 <= 10 then
    print("The number is less than or equal to 10.")
end

print("End of conditional.")
```

Running this will print out:

```
End of conditional.
```

Since the condition `15 <= 10` evaluates to `false`, the code block in the conditional statement is not ran.

# Else Statements

There are times where you want to execute different code depending on whether the condition evaluates to `true` or `false`. This is where the `else` statement comes in handy.

An **else statement** is a part of a conditional statement that will run a piece of code if the condition evaluates to `false`. Below is an example of how a conditional statement containing the `else` statement is structured:

```lua
if condition then
    -- Code to run if the condition is `true`
else
    -- Code to run if the condition is `false`
end
```

If `condition` evaluates to `true`, the code between `then` and `else` is executed. Otherwise, the code between `else` and `end` is executed.

Remember: There is only one `end` for the entire conditional statement.

Here is an example of a conditional statement containing an `else` statement:

```lua
local itemPrice = 20
local playerCoins = 50

if playerCoins >= itemPrice then
    print("You purchased the item.")
    playerCoins = playerCoins - itemPrice
else
    print("You cannot afford the item.")
end

print("Current number of coins: ")
print(playerCoins)
```

Running this will print out:

```
You purchased the item.
Current number of coins:
30
```

If `playerCoins` was set to something less than `itemPrice` (For example, 15), the following is printed out instead:

```
You cannot afford the item.
Current number of coins:
15
```

# ElseIf Statements

You might also want to evaluate multiple conditions and execute different code depending on which condition evaluates to `true`. This is where `elseif` statements come in!

An `elseif` statement is a part of a conditional statement that is ran if the previous condition above it evaluates to `false`. You can have as many `elseif` statements as you want.

Below is how a conditional statement containing `elseif` is structured:

```lua
if condition1 then
    -- Code to run if the condition1 is `true`
elseif condition2 then
    -- Code to run if condition2 is `true`
elseif condition3 then
    -- Code to run if condition3 is `true`
end
```

If any of the conditions evaluate to `true`, the corresponding block of code is executed, and the rest of the conditional statement is skipped.

You can also combine `elseif` with an `else` statement, which must be placed at the end:

```lua
if condition1 then
    -- Code to run if the condition1 is true
elseif condition2 then
    -- Code to run if condition2 is true
elseif condition3 then
    -- Code to run if condition3 is true
else
    -- Code to run if no other condition is true.
end
```

> ⚠️ **Placement of `else` Statements**
> The `else` statement must always be at the end of the conditional statement. Similarly, the `if` statement must be at the beginning. Placing them elsewhere will cause your code to error.

Here is an example of a conditional statement with `elseif` statements in action.

```lua
local itemName = "Technology"

if itemName == "Brimstone" then
    print("Brimstone shoots brimstone lasers.")
elseif itemName == "Technology" then
    print("Technology shoots generic lasers.")
else
    print("Could not recognize the item.")
end
```

Running this will print out:

```
Technology shoots generic lasers.
```

Changing `itemName` to "Brimstone" will print out:

```
Brimstone shoots brimstone lasers.
```

And any value for `itemName` would print:;

```
Could not recognize the item.
```

It's important to remember that having an `elseif` statement is not the same as having separate conditional statements. Consider the following:

```lua
local myValue = 90

if myValue > 50 then
    print("myValue is greater than 50!")
elseif myValue > 70 then
    print("myValue is greater than 70!")
end
```

Running this will output:

```
myValue is greater than 50!
```

Even though `myValue` is greater than both 50 and 70, once a single condition in a conditional statement evaluates to `true`, the rest of the conditions are not evaluated.

Now, consider the above example if it was broken to two separate conditional statements:

```lua
local myValue = 90

if myValue > 50 then
    print("myValue is greater than 50!")
end

if myValue > 70 then
    print("myValue is greater than 70!")
end
```

Running this will output:

```
myValue is greater than 50!
myValue is greater than 70!
```

# Quiz

Do not run any of these code snippets.

1.) What does this print?

```lua
local myBoolean = false

if myBoolean == false then
    print("myBoolean is false")
end
```

<details>
  <summary>Solution</summary>

```
myBoolean is false
```

Even though `myBoolean` is false, we are still checking to see if `myBoolean` is equal to false. As a result, the condition is evaluated as true and "myBoolean is false" is printed.

</details>
<br>

2.) What does this print?

```lua
local height = 10

if height >= 20 then
    print("You are tall!")
else
    print("You are too short.")
end
```

<details>
  <summary>Solution</summary>

```
You are too short.
```

</details>
<br>

3.) What does this print?

```lua
local coins = 50

if coins >= 40 then
    print("You are rich")
elseif coins >= 10 then
    print("You are well-off")
else
    print("You are broke")
end
```

<details>
  <summary>Solution</summary>

```
You are rich
```

</details>
<br>

4.) This is a trick one. It's okay if you don't understand this, we'll go over it more in the next section. What does this print?

```lua
local myNumber = 20

if myNumber >= 10 then
    if myNumber >= 20 then
        print("Foo")
    end

    print("Bar")
else
    print("Baz")
end
```

<details>
  <summary>Solution</summary>

```
Foo
Bar
```

We have a conditional statement inside a conditional statement. If `myNumber` is greater than or equal to 10, another conditional statement is ran inside, where we print out "Foo" if `myNumber` is greater than or equal to 20. "Bar" is printed to the console regardless of what the inner conditional statement is evaluated as.

</details>
<br>
