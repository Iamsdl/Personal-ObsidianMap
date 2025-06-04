Type safety is a feature of the language that you program in. Such languages can also be referred to as:
- _Strongly typed_ (vs _weakly typed_)
- _Statically typed_ (if types are checked at compile time)
- _Hard typed_ / _Soft typed_ (less common, informal terms)

> These terms are often used interchangeably, but they don’t always mean exactly the same thing. For example, _dynamic typing_ vs _static typing_ refers to **when** the type is checked, not **how strict** the typing is.

A **type safe** language prevents you from mixing values of the wrong [[Data and Variables#Data type|type]].
This helps catch mistakes early and improves reliability.
# Examples:
**Type safe** — _C#, Java, Rust_
```C#
int x = "hello";  // compile-time error
```

**Not type safe** — _JavaScript, Python_
```JS
x = 5;
x = "now a string";  // allowed
```