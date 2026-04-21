The `sealed` keyword can be seen as another [[Class access modifiers|class access modifier]]. It prevents a class from being inherited
```C#
public sealed SealedClass
{

}

//will give a compiler error because SealedClass is sealed
public InheritingClass : SealedClass 
{

}
```