Lambda expressions are the modern, concise way to create [[Anonymous functions|anonymous functions]].
A **lambda** uses the `=>` syntax. It can be used anywhere a delegate is expected. There's two ways of creating a function:
1. The short "expression" way
```C#
Func<int, int> f = x => x + 1;
```
2. The longer, "block body" way.
```C#
Action<string> log = s => { Console.WriteLine(s); };
```