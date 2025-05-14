### a. What is AMQP?
AMQP stands for Advanced Message Queuing Protocol. It is an open standard protocol for message-oriented middleware. AMQP enables systems to communicate by sending messages through queues, supporting reliable, asynchronous, and decoupled communication between distributed applications.

### b. What does guest:guest@localhost:5672 mean?

The first guest is the username for authentication.
The second guest is the password for authentication.
localhost is the hostname (the local machine).
5672 is the port number used by default for AMQP (RabbitMQ and similar brokers).
So, amqp://guest:guest@localhost:5672 is a connection string (URI) that tells your application to connect to an AMQP broker (like RabbitMQ) running on your local machine, using the username guest and password guest, on port 5672.
