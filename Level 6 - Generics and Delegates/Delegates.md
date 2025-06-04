I briefly mentioned in [[Operations, operators, and operands#Operands]] how [[Operations, operators, and operands#Operations|operations]] themselves can become [[Operations, operators, and operands#Operands|operands]]. Delegates are the feature that allows us to accomplish just that. They allow you to treat functions as values — to assign them to variables, pass them around, and invoke them later. I say "delegates", but there's two things here really.
# Delegate type
The **delegate type**, if it wasn't obvious enough from the name, is the [[Data and Variables#Data type|type]]. Similar to [[Classes|classes]], you first have to communicate to your computer that this type exists and describe what it looks like. This is a [[Instructions (statements)#Declarative statements|declarative statement]], and the syntax for it is `ReturnType` + `DelegateName` + `Parameters`. The [[Function signature|signature]], if you will, but it's not quite the same signature.
```C#
public delegate void Writer(string message);
```
> Note: delegates have the same [[Class access modifiers|access modifiers]] [[Classes|classes]] do.
# Delegate
The **delegate** is the [[Data and Variables#Variables|variable]]. 
The only difference from other variables is that it holds [[Functions|functions]] that match what the [[#Delegate type|delegate type]] specifies.
> A delegate can hold more than one function.

```C#
public void Main()
{
	Writer log = Console.WriteLine; //Notice the absence of "()". myDelegateName is not 
											   //assigned the result of WriteLine, it is assigned the 
											   //function itself.

	log += File.WriteLine; //Notice the "+=". Multiple functions can be added
									  // (or removed with -=) to the same delegate.

	log("Hello world"); //actual function call. This calls both Console.WriteLine() 
								   //and File.WriteLine()
}
```
> Note: A delegate can be overwritten, which brings us to the next topic:
# [[Events]]