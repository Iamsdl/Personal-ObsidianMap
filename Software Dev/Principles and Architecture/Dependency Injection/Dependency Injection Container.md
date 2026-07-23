A DI Container is [[Indirection]] applied to the [[Composition root]], and it becomes the [[Creator]] in GRASP. It is a class whose purpose is to manage dependencies and their lifetimes.
## Object Lifetime Scope
Lifetime Scope is extending the meaning that [[Data and Variables#Scope|Scope]] had for simple variables. The meaning shifts from "how long is a variable alive/visible" to "what kind of life should this dependency ([[Object|object]]/[[Classes|class]]) have". "Life" here means "[[Clearing up confusing terminology|instancing]] strategy":
- [[Singleton|Singleton]] = The same [[Clearing up confusing terminology|instance]] for all classes
- Scoped = A different [[Clearing up confusing terminology|instance]] per "scope" (scope here can mean a web request, an event handler, whatever else. It depends on your context)
- Transient = A different [[Clearing up confusing terminology|instance]] for all classes