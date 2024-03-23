**Comments** are human-readable notes that you include in your code. They are extremely useful for making your code easier to understand for both yourself and others who may read it.

Creating comments in Lua is very easy. To create a **single-line** comment, use `--.` Anything you type to the right of `--` on the same line will be ignored by the game. Here's an example:

```lua
-- I am a comment!
```

When a Lua script runs, whitespaces and comments are ignored:

```lua
-- print("Hello World!") -- Nothing printed because it's a comment!
```

Lua also supports **multi-line comments**. These can span multiple lines, making it easy to comment out larger blocks of code or write more detailed explanations. To create a multi-line comment, use `--[[` and `]]`:

```lua
--[[
    Hello, World!

    I can extend multiple lines quite easily.

            Pretty neat, huh?
]]
```

Everything between the `--[[` and `]]` markers will be treated as a comment.