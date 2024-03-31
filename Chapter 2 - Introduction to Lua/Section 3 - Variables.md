# Introduction to Variables

When coding, you will often need to store values and access them later. For example, you might want to track the total number of coins collected in a run or the number of times you've defeated a specific enemy. This is where variables come on!

A **variable** is a named object that stores a value. Declaring (creating) a variable in Lua is straightforward.

```lua
local greeting = "Hello World!"
```

Let's break down the code:

- `local`: The `local` keyword indicates that the variable is **locally scoped**. We'll discuss scope in detail in a later section, but for now, remember to always include it!
- `greeting`: This is the name of the variable. We've chosen it to be "greeting".
- `=`: This is the **assignment operator**. The assignment operator assigns the value on the right-hand side to the left-hand side.
- `"Hello World!"`: This is the value assigned to the variable.
  
In summary, we've declared a variable named "greeting" and assigned it the value "Hello World!".

The next step is to access the variable. We can do this by simply using the variable's name:

```lua
local greeting = "Hello World!" -- Declare a variable named "Hello World!"
print(greeting) -- Print out the value of the variable `greeting`
```

Running this script will print "Hello World!" to the console. Congratulations, you declared your first variable and accessed it!

It's important to know that variable names are case-sensitive. Consider the following example:

```lua
local coolVariable = "This is a cool variable!"
print(CoolVariable)
```

This code will print "nil" instead of "This is a cool variable!". This is because we haven't declared a variable named `CoolVariable` (notice the capital C). While most coding languages will immediately throw an error telling you that the variable does not exist, Lua does not do that. This makes typos like this particularly dangerous, as they can lead to unexpected bugs.

When declaring a variable, you don't need to assign it a value immediately:

```lua
local coolVariable
print(coolVariable) -- Prints "nil"
```

This prints `nil` because although we declared the variable `coolVariable`, we haven't assigned it any value.

You can also change the value of a variable later on in your code:

```lua
local myVariable = "Hello World!" -- Declare `myVariable` with a value of "Hello World!" 
print(myVariable) -- Prints "Hello World!"
myVariable = "Goodbye World!" -- Change the value of `myVariable` to "Goodbye World!"
print(myVariable) -- Prints "Goodbye World!"
```

Notice that we didn't use `local` when changing the value on the third line. This is because we already declared the variable on the first line. Using `local` again would create a new, separate variable with the same name. While this doesn't make a difference in simple examples such as this, it can lead to unexpected problems in more complex code. We'll discuss this further in a later section.


> **⚠️ Remember**
> Only include `local` when **creating** a variable. Don't use it when accessing or changing the variable's value.

You can also have multiple variables and assign the value of one variable to another:

```lua
local juice = "Juice!" -- Declare `juice` with a value of "Juice!"
local fruit = "Fruit!" -- Declare `fruit` with a value of "Fruit!"

fruit = juice -- Change the value of `fruit` to the value of `juice`, which is "Juice!"
print(fruit) -- Prints "Juice!"
```

Another point to know is that you can declare multiple variables in one line:

```lua
local a, b
```

This code creates two local variables, `a` and `b`. You can also assign values to them directly:

```lua
local a, b = "Hello", "World"
```

Just like the variables, each value would need to be separated by a comma. In this case, "Hello" would be assigned to `a` and "World" would be assigned to `b`.

> ✨ **Avoid Declaring Multiple Variables in a Single Line**
> While allowed, declaring multiple variables in a single line can make your code harder to read and understand. Stick to declaring one variable per line for better clarity.

# Variable Naming Rules

When naming variables in Lua, you must follow certain rules. Violating these rules will cause your code to error.

## No Special Characters

Variable names can only consist of the following characters:
- Uppercase and lowercase English letters.
- Numbers.
- Underscore (`_`).

Any other characters, such as `!`, `-`, or spaces are not allowed.

**❌ Bad**

```lua
local my-variable1 = "Hello World!"
local my variable2 = "Hello World!"
local myvariable3! = "Hello World!"
```

**✅ Good**

```lua
local my_variable1 = "Hello World!"
local myVariable_2 = "Hello World!"
local _myVariable3 = "Hello World!"
```

## No Numbers as the First Character

Variable names cannot start with a number.

**❌ Bad**

```lua
local 1Variable = "Hello World!"
local 2Plus2 = "Four"
```

**✅ Good**

```lua
local variable1 = "Hello World!"
local TwoPlusTwo = "Four"
```

## No Lua Reserved Keywords

Variable names cannot be the same as Lua's reserved keywords. Here's a list of reserved keywords:

- and
- break
- do
- else
- elseif
- end
- false
- for
- function
- if
- in
- local
- nil
- not
- or
- repeat
- return
- then
- true
- until
- while


While you could technically circumvent this by changing the case of the keyword (e.g., using `True` instead of `true`), this is strongly discouraged as it can lead to confusion.

## Give Variables Clear Names

"There are only two hard things in Computer Science: cache invalidation and naming things." -- Phil Karlton

While not enforced by Lua, giving your variables clear and descriptive names is arguably the most important rule to follow.

Consider the following examples:

```lua
local x = "Hello World!"
-- Or...
local greeting = "Hello World!"
```

Which variable name makes it clearer what the variable represents? Clearly, `greeting` is a better choice. When naming variables, choose names that reflect their purpose. Using random or unhelpful names will make your code harder to understand for both yourself and others.

# Quiz

**For this quiz, do not run the code snippets!**

1.) What does the following code print? 

```lua
local myVariable = "Hello!"
print(myVariable)
```

<details>
  <summary>Solution</summary>
  "Hello!"
</details>
<br>

2.) What does the following code print?

```lua
local myVariable = "Hello!"
myVariable = "How are you?"
print(myVariable)
```

<details>
  <summary>Solution</summary>
  "How are you?"
</details>
<br>

3.) What does the following code print?

```lua
local myVariable = "Hello World!"
print(myvariable)
```

<details>
<summary>Solution</summary>
nil
</details>
<br>

4.) What does the following code print?

```lua
local variable1 = "Hello World!"
local variable2 = "Goodbye World!"
variable2 = variable1
print(variable2)
```

<details>
<summary>Solution</summary>
"Hello World!"
</details>
<br>

5.) This is a trick one. Write a code snippet that declares a variable named "best_item" and give it a value of the name of your favorite item! Then, print out "The best item in the game is: " followed with the value of the variable.

<details>
<summary>Solution</summary>

```lua
local best_item = "Bob's Rotten Head"
print("The best item in the game is:")
print(best_item)
```
</details>
<br>