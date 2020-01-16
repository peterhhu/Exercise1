# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is when multiple computations can start, run and complete
   in overlapping time periods.
   The techniques make programs more usable.
 > Parallellism is a technique used to make programs faster by performing
   multiple computations at the same time (in parallell).
 > The difference is that parallellism is physically dependent while concurrency
   can be realized solely through programming (not dependent of the physical multiplicity).
   So there might be concurrency without parallelism. 
 
 ### Why have machines become increasingly multicore in the past decade?
 > Machines have become increasingly multicore due to the necessity of 
   fast computation. The single cores have met their limitation compared to the multicore.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Decreasing waiting time, due to the fact that computations are executed concurrently.
   Decreasing response time
   Increases efficiency
   Increases resource utilization
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > Creating concurrent programs may be easier when one know how concurrency is supposed to work, but concurrency adds a lot of extra syntax and programming techniques that a programmer need to be aware of. So both easier and harder is the diplomatic answer. 
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > A process is the instance of a computer program that is being executed by one or many threads.
   A process, depending on the OS, may be made up of multiple threads which execute instructions concurrently.
 > A thread is a part of a program that has split itself into two or more pieces (threads). Each thread runs its
   part/task of the program concurrently.
 > A green thread is scheduled by a runtime library or virtual machine instead of the OS.
 > A coroutine is very similar to a thread, but they are cooperatively multitasked.
   That means they provide concurrency, but no parallelism.They are not OS-managed
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > Threads
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > The Python GIL is a lock that allows only one thread to hold the control of the Python interpreter.
 > This then assures that only one thread can be in a state of execution at any point in time.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Multiprocessing module instead of multithreading, creating processes each with its own interpreter,
   allowing concurrency on multicore processors.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > "func GOMAXPROCS(n int) int" sets the maximum number of CPUs that can be executing simultaneously
   and returns the previous setting.
