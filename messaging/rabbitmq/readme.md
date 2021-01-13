# Rabbitmq

## Architecture

- Implementation of AMQP (Advanced messagig Queing Protocol)

### Characteristics
* Cloud friendly: installed using docker container / helm chart etc., 
* Cross-language compatibility: Producer can be in Go and consumer can be in Javascript
* Security: supports LDAP, ssl and tls. 
* Message acknowledgements: Message will be in the queue till the consumer acknowledges the receipt of the message
* Good management console: 

### Terms
* Producer/consumer/Queues
* Exchanges

#### Other terms:
* Routing key

### Exchanges

#### Exchange types
* Fanout: exchange will duplicate the message to all queues it knows about. 
* Direct: 
    - Producer creates a routing key with the message 
    - Exchange sends it to any queue whose binding key matches with the routing key. 
* Topic: 
    - Producer creates a routing key - say "ship.shoes"
    - Exchange will map to any queue with appropriate binding key "ship.any" supported
* Header:
    - Routing key is ignored.
    - Routed to queues using the header. 
* Default:
    - Routing key is mapped directly to the queue name. 



