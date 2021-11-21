# Thread and Processes

## 1-) Threads
 a thread is a computation process that is to be performed by a computer. It is a sequence of such instructions within a program that can be executed independently of other codes.
[**cpu_waster_thread.py**](https://github.com/yunusaltuntas/Parallel_Programming/blob/main/Treads%20and%20Processes/cpu_waster_thread.py) is example of thread.
 - Threads are like mini-processes that live inside a process
 - They share memory space and efficiently read and write to the same variables
 - Two threads cannot execute code simultaneously in the same python program

 
## 2-) Processes
 A process is an instance of program.Processes spawn threads (sub-processes) to handle subtasks.
[**cpu_waster_process.py**](https://github.com/yunusaltuntas/Parallel_Programming/blob/main/Treads%20and%20Processes/cpu_waster_process.py)  is example of process.
 - Created by the operating system to run programs
 - Processes can have multiple threads
 - Two processes can execute code simultaneously in the same python program
 - Processes have more overhead than threads as opening and closing processes takes more time
 - Sharing information between processes is slower than sharing between threads as processes do not share memory space. In python they share information by pickling data structures like arrays which requires IO time.

## Other Scripts
- [**scheduling.py**]() => in this project has example of thread work until time is up
- [**thread_lifecycle.py**]() => in here, we can understand basically when do threads wait and then threads work
- [**deamon_thread.py**]() => in this example, sometimes the main thread finish but our program can still work this may cause a problem. this problem has a solution here. 
if you define daemon thread. when the main thread finishes, automatically will close the daemon thread
- [**data_race**]() => A race condition occurs when two or more threads can access shared data and they try to change it at the same time. As a result, the values of variables may be unpredictable and vary depending on the timings of context switches of the processes.
- [**mutual_exclusion.py**]() => Mutual exclusion is the ability of a program to control access to a shared resource. It is the ability of a program to ensure that only one thread at a time can access a shared resource.
- [**reentrant_lock.py**]() => Reentrant lock is a lock that can be acquired multiple times by the same thread.
- [**nonblocking_acquire.py**]() => when one thread blocks a critical section another thread waits to get that. in these times, the thread can do something. this's name is nonblocking acquire. this example has a nonblocking acquire
- [**read_write_lock.py**]() => in this script has solved the read-write problem. The previous examples had mutex solutions to access the shared resource, but in many thread reader and writer problems, one reader waits for another to read. this was not logical because shared resources don't change in reading it changes only writing so reading thread should work concurrently. the read-write-lock library solves this problem
- [**deadlock.py**]() => in this script, there are three threads. The first thread gets acquire chopstick_a  and second is  chopstick_b and the third is chopstick_c. however, the first thread needs to continue chopstick_b. and the second thread needs to continue chopstick_c. the third thread needs to continue chopstick_a.  all threads need others to continue. this problem causes deadlock occurs.