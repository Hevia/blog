# Introduction
One of the best next steps you can take on your Python journey is diving into concurrency & parallelsim. Many developers will often learn enough to get by, 
but you can spend your entire career in this space! There are a lot of exciting things to learn, but newcomers can often feel intimadated by the steep curve. 
In this series of short posts I am hoping we can distill these topics so you can start writing more performant Python 🚀🐍


## Concurrency vs Parallelism
When starting out in this space, these two terms can often cause some confusion. So let's quickly define them:

| Paradigm      | Definition |
| ----------- | ----------- |
| Concurrency      | The process of interleaving individual tasks one at a time within bits of code (tasks being individual pieces of work i.e: adding together two numbers or sending a network request).|
| Parallelism   | Exectuing several or more bits of code at the same time.|



For a more descriptive analogy. You can think of parallelism as a grocery store with multiple checkout lanes. 
Customers (the code) don't all have to use the same lane to have their goods processed. You can think of concurrency, as yourself! 
Maybe while you wait for your coffee to brew, you read the bird app, or while your code is building you go off and reply to emails

[TODO: Drawing]

## CPU vs IO workloads
To fully take advantage of the performance benefits that come with concurrent/parallel code. You need to know when to use what technique. Luckily figuring out isn't too bad. 
Generally the advice for most situations goes like this:

For CPU workloads, you'll want to use Parallelim/Processes
For IO workloads, you'll want to use Concurrency/Threads

But what exactly is the distinction between these two workloads? Back to the terminology!

| Workload      | Definition |
| ----------- | ----------- |
| CPU      | Math, running methods on some data, physics simulation, running game AI.       |
| IO   | Reading/Writing data from disk, sending/reciving network data.        |

If you're feeling confused, don't worry! We'll go deeper in a moment. 

# Threads
Threads are

```
code snippet here
```

## Oh My GIL
The reason only one thread can run at a time in Python is thanks to the Global Interpreter Lock (GIL). While many cite the GIL as the source of all their problems, 
working with multiple threads in large applications is *hard*. Writing multithreaded code introduces a whole new slew of bugs such as data races, deadlocking, & heseinbugs. 
The GIL is saving your future self a lot of time. 


# Processes
Every time you run Python it spawns its own "process". The process handles state & lots of other things you the programmer doesn't need to worry about. As stated above each process comes with its own GIL

```
code snippet here
```

Hopefully you can see why this is useful here. Most languages don't have a GIL 

# Conclusion
We covered a lot of ground! Luckily this is as about as dense as it gets for awhile. As you dig deeper the nuances start to show, but the overview is enough to help you take the leap. 

To review:
- In any given Python process, only one thread can run at a time due to the Global Interprter Lock (GIL)
- Threads are lightweight and a good choice for I/O workloads
- Whenever you start a Python program it starts its own process with its own thread pool + GIL. You can spawn additional processes which are a good way to speed up CPU workloads

In later posts we'll explore other topics such as async/await, coroutines, getting past the GIL, and more.


# References
- https://python.hamel.dev/concurrency/
- https://realpython.com/python-concurrency/


