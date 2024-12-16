# Lua pairs iterator unexpected behavior with recursive table modification

This repository demonstrates a potential issue with Lua's `pairs` iterator when used with recursive functions that modify the table being iterated over.

## Bug Description

The provided Lua code recursively iterates through a nested table.  If the table structure is modified within the iteration, the `pairs` iterator may skip elements or behave unexpectedly.

## Reproduction

1. Clone this repository.
2. Run `bug.lua`.
3. Observe the unexpected output.

## Solution

The solution provided in `bugSolution.lua` addresses the issue by creating a copy of the table before iteration, ensuring that modifications do not affect the iteration process itself.