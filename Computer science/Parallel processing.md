Going into a bit more details regarding how things happen, there's a few levels:
# Cores
At the hardware level the [[Computer (CPU)|CPU]] is split into **cores**. It's just multiple processors linked together.
# Processes
A core can run processes. Managing this is mostly the operating systems responsibility. 
# Threads
A process can start different **execution threads**. A thread is a "unit of work" that is processed in parallel. 
If the CPU has multiple cores, a thread will be executed on another core and be "truly parallel", otherwise
If the CPU does not have multiple cores, it will alternate between the threads, processing a bit of each at a time.
  > Note: This is actually how the computer always runs. It switches between processes/threads all the time, but it happens so fast you don't notice it.