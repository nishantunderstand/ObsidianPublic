Architectural Style 
1. Monolithic : Method Call
2. Microservice : 

Communication / Protocols 
1. Sync (REST API) 
2. Async (RabbitMQ, KAFKA)

Sync :  REST API ,HTTP / HTTPS, 
RestTemplate, RestClient, **FeignClient**
WebClient  (Related to Spring Reactive Mono/Flux)
https://www.youtube.com/watch?v=Y6irJSRX4zk

AMQP and HTTP Protocols    
HTTP vs HTTPs

AMQP 
1. Advanced Message Queuing Protocol
2. Famosuly Used for RabbitMQ

How this is service communication ? 
Communication is between user or system ?

```
COMMUNICATION IN MICROSERVICE ARCHITECTURE
│
├── 1. Client → Service
│   │
│   ├── Client
│   │   ├── Browser
│   │   ├── Mobile App
│   │   ├── Postman
│   │   └── External System
│   │
│   └── Usually: HTTP / HTTPS
│
├── 2. Service → Service
│   │
│   ├── Synchronous
│   │   ├── REST API
│   │   ├── Feign Client
│   │   └── WebClient
│   │
│   └── Asynchronous
│       ├── Kafka
│       └── RabbitMQ
│
└── Protocols
    │
    ├── HTTP / HTTPS
    │   └── Used by REST APIs
    │
    ├── Kafka Protocol
    │   └── Used by Apache Kafka
    │
    └── AMQP
        └── Advanced Message Queuing Protocol
            └── Commonly used with RabbitMQ
```