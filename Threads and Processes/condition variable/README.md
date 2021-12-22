# Condition Variable

[**condition_variable.py**]() ==> in this example, there are two hungry people. they should eat with sequence. if it's not in her turn. it tries again to eat until her sequence So it wastes her time. you can see this problem here
[**condition_variable_for_two_thread.py**] ==> here is a solution. when one thread executes that sends a wait signal to another thread. when the thread finishes the execution, that sends wake up signal and the other thread start to execute so it is more efficiently from first
[**condition_variable_for_many_thread.py**] ==> above solution send only to one thread wait signal or wake up signal. if there are many threads to send wait signal and wake up signal  in that changes only from "notify" to "notify_all"