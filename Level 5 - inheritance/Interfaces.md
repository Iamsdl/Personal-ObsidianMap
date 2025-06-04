Interfaces are... a weird thing.  
Conceptually, interfaces represent a **contract** or **capability**. An interface says: "Any class that implements me must have these members."
Functionally, they're like a [[Overriding#abstract|purely abstract class]] — they define members without implementations — but they come with some key differences: 
- interfaces support **multiple inheritance**.
(since they represent contracts) **all interface members are [[Members access modifiers|public]] and must be implemented as public**

> A class doesn't **inherit** an interface — it **implements** it.
```C#
interface IDriveable {
    void Drive();
}

class Car : IDriveable {
    public void Drive() {
        Console.WriteLine("Vroom!");
    }
}
```