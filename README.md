## REFLECTION
1. **How many data your publisher program will send to the message broker in one run?**
> Five messages per run, as there is five calls of the method publish_event sending UserCreatedEventMessage to the broker.
2. **The url of: "amqp://guest:guest@localhost:5672" is the same as in the subscriber program, what does it mean?**
>The two programs connects to the same AMQP (Advanced Message Queueing Protocol), using also the same credentials (guest:guest) with the server being located in localhost port 5672.
<br>

### **Screenshot of first running RabbitMQ:**
![alt text](images/running_rabbitMQ.png) <br><br>

### **Screenshot of publisher console running cargo run, sending five events to the message broker.**
![alt text](images/terminal_publisher.png) <br><br>

### **Screenshot of subscriber console receiving five events from the publisher.**
![alt text](images/terminal_subscriber.png) <br><br>

### **Screenshot of RabbitMQ Message Rates graph spiking due to the publisher sending messages to the message broker. Graph shows the rate at which messages are entering the server.**
![alt text](images/spike_rabbitMQ.png) <br><br>