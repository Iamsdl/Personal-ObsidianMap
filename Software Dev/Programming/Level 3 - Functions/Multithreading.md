As the name implies, multithreading is the act of using multiple [[Parallel processing#Threads|threads]] in a program.

When writing multithreaded programs, you need to be careful with concurrent access. 
This means two threads accessing the same [[Data and Variables|variable]] at the same time.

You can avoid concurrency issues by using the `lock` keyword. It locks a resource (variable) so other threads that try to access it will have to wait until the first thread is done with it's work.
# Example:
```C#
int x = 0;

void Add1()
{
	//any object can be locked, really
	//usually a dedicated "lock" object is created
	lock(x) 
	{
		x = x + 1;
	}
}

void Main()
{
	Thread myThread1 = new Thread(new ThreadStart(Add1));
	Thread myThread2 = new Thread(new ThreadStart(Add1));
	myThread1.Start();
	myThread2.Start();
	//x will be 2 here.
}
```
There is one big problem with locking, and that is when Thread1 is waiting for Thread2 and Thread2 is waiting for Thread1. This is known as [[Deadlock|deadlock]].