# producer consumer

in this example we will use a queue to simulate a producer-consumer problem 
when a producer is adding items to the queue and a consumer is removing them.
while one thread will produce items and the other two threads will consume them.
for this example, if we use one consumer, queue can explode. the producer can produce more than consumer consumption . and queue swell up .so the average rate of consumer should be bigger than  average rate of producer