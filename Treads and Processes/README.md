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
- 