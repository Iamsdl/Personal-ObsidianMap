**Reflection** is the ability of a program to inspect itself while running.
It lets you look at:
- All [[Classes|classes]], [[Functions|functions]], [[Properties|properties]] in an assembly
- The [[Data and Variables#Data type|types]] of [[Data and Variables#Variables|variables]] at runtime
- What [[Attributes|attributes]] are applied
```C#
Type type = typeof(MyClass);
var methods = type.GetMethods();
var attrs = type.GetCustomAttributes(false);
```
> In short: **Reflection** is how you read the metadata — **Attributes** are just one kind of metadata.