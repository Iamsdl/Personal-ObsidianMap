# Operations
An **operation** represents any kind of action or process.

An operation may:
- Use [[#Operands|operands]] (things it acts upon)
- Produce a result or have side effects
- Be implemented as code (in programming), or occur in the real world (e.g., stacking boxes)

Examples:
- **Walking** is an operation without operands and without results (just motion).
- **Cutting** is an operation that uses operands and produces a result.
  - e.g., Cutting a pear (operand) → produces pear slices (result).
## Operators
An **operator** is a special kind of [[#Operations|operation]] that uses a **symbol** instead of a name to represent it.

- Common in both mathematics and programming.
- Operators always have a result.
- They typically act on one or more [[#Operands|operands]].
  - `+` is an operator for the addition operation.
  - `*`, `/`, `-`, `==`, `!`, and so on.

Operators are the symbolic interface to operations.
# Operands
An **operand** is a value or object that an [[#Operations|operation]] or [[#Operators|operator]] acts upon.
Examples:
- In `2 + 3`, both `2` and `3` are operands.
- In "cutting a pear", the pear is the operand.
> Operations can sometimes *become* operands themselves.  
> Example: In `f(g(x))`, `g(x)` is a function invocation used as an operand for `f`.

> In practice, since anything can become an operand for the right operation, operands are referred to as [[Object|objects]].