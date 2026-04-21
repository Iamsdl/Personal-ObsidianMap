Basic [[Operations, operators, and operands#Operation|operations]] are provided out of the box and are the building blocks of everything else.
They are:
# Arithmetic operations
Arithmetic operations take two [[Basic Data Types#The numbers|numbers]] as input and have another [[Basic Data Types#The numbers|number]] as output.
They are:
- `+` -> Addition
- `-` -> Subtraction
- `*` -> Multiplication
- `/` -> Division
- `%` -> Modulo (returns the remainder of the division)

> Note, as they use symbols, these are [[Operations, operators, and operands|operators]].

> The math involving [[Basic Data Types#The numbers|numbers]] is called [[Algebra]].
## Examples
```C#
1 + 1; // = 2
5 - 3; // = 2
2 * 3; // = 6
6 / 2; // = 3

7 / 2; // = 3 because of truncation
7 % 2; // = 1

7.0 / 2; // = 3.5
```
# Logical operations
Logical operations take two [[Basic Data Types#The boolean|booleans]] as input and have another [[Basic Data Types#The boolean|boolean]] as output.
They are:
- `&&` -> AND
- `||` -> OR
- `!` -> NOT
- `^` -> XOR (exclusive OR)
Note, as they use symbols, these are [[Operations, operators, and operands|operators]].
The math involving [[Basic Data Types#The boolean|booleans]] is called [[Boolean Algebra|boolean algebra]].
## Examples
```C#
true && true; //true
true && false; //false
false && false; //false
```

# Comparison operations
Comparison operations take any two [[Object|objects]] (usually [[Basic Data Types#The numbers|numbers]]) as input and have a [[Basic Data Types|boolean]] as output.
They are:
- `==` -> Equals
- `!=` or `<>` -> Not Equals
- `<` and `<=` -> Less than, Less than or equal
- `>` and `>=` -> Greater than, Greater than or equal
Note, as they use symbols, these are [[Operations, operators, and operands|operators]].
# String operations
[[Basic Data Types#The string|String]] operations are basic operations only because they are provided out of the box by every programming language. They are actually [[Functions|functions]].
Examples include: concatenation, comparison, replacing part of a string with another, trimming, searching, splitting, joining, etc.
# Collection operations
[[Basic Data Types#Collections|Collection]] operations are basic operations only because they are provided out of the box by every programming language. They are actually [[Functions|functions]]
Examples include: Adding, removing, iterating, sorting, filtering, mapping, etc.