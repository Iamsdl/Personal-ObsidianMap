Basic [[Data and Variables|data types]] are provided out of the box and are the building blocks for everything else.
They are:
# The boolean
The boolean is a type used to represent `true` and `false`.
May be treated as a [[Basic Data Types#The numbers|number]], with 1 being true and 0 being false.
For operations, see [[Basic operations#Logical operations|logical operations]].

*The math involving [[Basic Data Types#The boolean|booleans]] is called [[Boolean Algebra|boolean algebra]].*
# The numbers
Love 'em, hate 'em, you need 'em.
Numbers are broken down into:
- signed integers = [[Number sets#Natural numbers|natural]] numbers
- unsigned integers = [[Number sets#Integer numbers|integer]] numbers
- floating point = [[Number sets#Rational numbers|rational]] and [[Number sets#Irrational numbers|irrational]] numbers

|         | Signed integers | Unsigned integers | Floating point |
| ------- | --------------- | ----------------- | -------------- |
| 8 bit   | sbyte           | byte              |                |
| 16 bit  | short           | ushort            | half           |
| 32 bit  | int             | uint              | float          |
| 64 bit  | long            | ulong             | double         |
| 128 bit |                 |                   | decimal        |
For operations, see [[Basic operations#Arithmetic operations|arithmetic operations]].

*The math involving [[Basic Data Types#The numbers|numbers]] is called [[Algebra]].*
# The char
A char is a letter. Specifically it represents a character from the [[ASCII table]]. 
A char may be treated as a [[Basic Data Types#The numbers|byte]].
# The string
If a [[Basic Data Types#The char|char]] is one character, a string is many characters (AKA text).
The string is a basic data type only because it is provided out of the box by every programming language. The string is actually a [[Classes|class]]. Specifically, it is an [[Immutable|immutable]] [[#Collections|collection]] of [[#The char|chars]].
# Collections
Collections are a [[Basic Data Types|basic data type]] only because they are provided out of the box by every programming language. Collections are actually [[Generics|generic]] [[Classes|classes]] used to hold many [[Object|objects]] of the same type.