# Reflection Publisher

# a. How much data your publisher program will send to the message broker in one run?
In a single run, the publisher program will send exactly five messages to the message broker. These messages are published as "user_created" events utilizing the UserCreatedEventMessage struct, with each message containing a sequential user_id from "1" to "5" and a corresponding user_name customized with your NPM (Amir, Budi, Cica, Dira, and Emir).

# b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
The identical URL indicates that both the publisher and subscriber programs are communicating through the exact same local message broker (RabbitMQ) instance. This shared connection is a fundamental requirement in message queuing architecture, as the subscriber must listen to the exact same server, port, and channel where the publisher is sending its data in order to successfully receive and process those messages.

![alt text](image.png) -> running rabbitMQ as message broker