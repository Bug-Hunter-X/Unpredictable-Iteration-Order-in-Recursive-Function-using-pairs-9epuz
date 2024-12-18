# Unpredictable Iteration Order in Recursive Function using pairs
This repository demonstrates a potential issue with Lua's `pairs` iterator when used in recursive functions. The issue stems from the fact that `pairs` does not guarantee a specific iteration order, leading to unpredictable results in certain scenarios.

## Bug Description
The provided Lua code uses a recursive function `foo` that iterates through a nested table using `pairs`. Due to the unpredictable iteration order of `pairs`, the function's behavior might vary between different Lua implementations or even between different runs of the same code. This can make debugging and maintaining the code challenging.

## Solution
The solution involves using a specific iteration order, such as iterating over keys in sorted order, to ensure consistent behavior.