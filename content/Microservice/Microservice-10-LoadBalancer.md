
Architectural Style 
1. Monolithic
2. Microservice

LoadBalancer
  
1. Client Side LoadBalancer  : Spring Cloud LoadBalancer
2. Server Side LoadBalancer : NGINX, AWS ALB
  
Load :  Incoming Traffic  / Request

Service Discovery vs Load Balancer

If I have 3 Order Service instances, who tells me their IP addresses?
Who decides which instance gets the request?

Can Service Discovery distribute traffic?
Can Load Balancer work without Service Discovery?
1. Static Load Balancing  : Fixed List
2. Dynamic Load Balancing  : Dymanic List

LoadBalancer vs API GateWay 

API Gateway + Load Balancer  
Is API Gateway a Load Balancer?


[Load Balancer](obsidian://open?vault=studywithmeHLD&file=LoadBalancer) 



1. WHERE are the instances? : Service Discovery
2. WHICH instance should receive the request? : Load Balancing
3. HOW should external clients enter and be routed? : API Gateway



Service Discovery vs Service Registration

Service Registration : "WHO are you?" "Where are you?" "Please add me to the registry."

Service Discovery : "Where is Order-Service?"