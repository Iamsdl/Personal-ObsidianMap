Generics are [[Functions|functions]] or [[Data and Variables#Data type|types]] ([[Classes|classes]]) not caring what they work with. They let you write code that works for _any_ type, without rewriting it for each one.
> You can recognize a generic by the angle brackets syntax: `<T>`

A common use of generics is in [[Basic Data Types#Collections|collections]] like `List<T>` or `Dictionary<TKey, TValue>`.
# Example - a stack
Here's a very basic implementation of a Stack.
```C#
public class Stack<T>
{
	private class Node<T>
	{
		public T Data { get; set; }
		public Node<T> Next { get; set; }
		
		public Node(T data, Node next)
		{
			Data = data;
			Next = next;
		}
	}
	
	private Node<T> top;
	
	public void Add(T data)
	{
		top = new Node(data, top);
	}
	
	public T Remove()
	{
		if (top == null)
			throw new InvalidOperationException("Stack is empty");
		
		T result = top.Data;
		top = top.Next;
		return result;
	}
}

public void Main()
{
	Stack<int> myStack = new Stack<int>();
	myStack.Add(1);
	myStack.Add(2);
	myStack.Add(3);
	myStack.Add(4);
	int x = myStack.Remove(); //4
	myStack.Add(5);
	//myStack will be [1, 2, 3, 5]
}
```