Class members are variables or functions defined inside a class. They are:
- [[Data and Variables#Variables|fields]]
- [[Getters and Setters|properties]]
- [[Methods|methods]]
- [[Constructors|constructors]]
- [[Destructors|destructors]]
- [[Operator overloading|operators]]
- [[Casts|casts]]
# Defining a member
This will be detailed in each section separately.
# Using a member
## From outside the class definition
With the exception of [[Constructors|constructors]] (which are used to create an [[Clearing up confusing terminology|instance]]), all [[Members access modifiers|accessible]] members are accessed with a dot, through an [[Clearing up confusing terminology|instance]].
## From inside the class definition
Since there is no [[Clearing up confusing terminology|instance]] yet, [[Members access modifiers|accessible]] members are accessed with a dot, through the `this` keyword.
> Note: Most of the time the `this` keyword can be omitted if there's no ambiguity.