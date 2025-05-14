### a. What is AMQP?
AMQP stands for Advanced Message Queuing Protocol. It is an open standard protocol for message-oriented middleware. AMQP enables systems to communicate by sending messages through queues, supporting reliable, asynchronous, and decoupled communication between distributed applications.

### b. What does guest:guest@localhost:5672 mean?

The first guest is the username for authentication.
The second guest is the password for authentication.
localhost is the hostname (the local machine).
5672 is the port number used by default for AMQP (RabbitMQ and similar brokers).
So, amqp://guest:guest@localhost:5672 is a connection string (URI) that tells your application to connect to an AMQP broker (like RabbitMQ) running on your local machine, using the username guest and password guest, on port 5672.

- Simulation slow subscriber
    ![alt text](img/image1.png)
    The queue held up to 20 messages on my system because the publisher sent messages faster than the subscriber could process them. This caused messages to build up in the queue until the subscriber eventually processed each one.

- Reflection and Running at least three subscribers
    ![alt text](img/image.png)
    The queue briefly peaked at 13 messages, then quickly dropped to 0. This happened because the publisher sent multiple messages, because there is 3 subscriber, the message can be processed parallely making run faster.