# message-ordering-in-distributed-system-using-logical-clock
Implement a system where messages between processes will be ordered according to 1. Fifo Ordering using vector clock 2. Causel Ordering using vector clock 3. total ordering using vector clock

#FIFO ORDERING


Language-Python.
With FIFO ordering, messages from process Pi must be received at each process Pj in the order the
messages were sent. In order to simulate the real world network message passing with delay. We have
implemented the program as follows.
1. At the start Multiple client will be connected to server.
2. Each client can send different no of message to other and for each message there will be a particular
threads which is responsible to sending the message.
3. Since the threads run in parallel so any message can be sent first like m5 can reach before m1.
4. Client send message with process id and vector clock.
5. At received side it checked to see if it the next expected msg.
6. If so the msg is accepted otherwise the msg is buffered.
7. The buffered msg will be procced later to accept already received msgs.

