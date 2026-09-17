Architectural Style 
1. Monolithic
2. Microservice

Why API Gateway ?

API Gateway vs Direct client-to-service communication
Centralized Entry Point

It handles 
1. routing
2. authentication
3. logging monitoring
4. rate limiting API versioning and load balancing.

Cross-Cutting Concern :
A. Traffic Management
1. Routing
2. Load Balancing
3. Rate Limiting
4. Circuit Breaking
5. Caching

B. Security
1. Authentication
2. Authorization
3. SSL/TLS Termination
4. CORS

C. Request/Response Processing
1. Request Transformation
2. Response Transformation
3. Request Aggregation
4. API Versioning

D. Observability
1. Logging
2. Metrics
3. Distributed Tracing

>North-South = traffic entering/leaving your system.
>East-West = traffic between services inside your system.


Types :
1. Client Side Gateway
2. Server Side Gateway

Popular API Gateway Products
OpenSource: 
1. Kong
2. NGINX
3. Spring Cloud Gateway

Enterprise
1. Apigee

Single Point of Failure
Can API Gateway and Load Balancer be used together?
API Gateway vs Load Balancer
LoadBalancer + Scaling 

Is API Gateway a Single Point of Failure? 

Anything Offered by AWS i.e. AWS API Gateway
Anything Offered by Redhat i.e. 3Scale API Managment

API Gateway + LoadBalancer 
API Gateway + ServiceDiscovery
API Gateway + Authentication Server : Keycloak, OAuth2
API Gateway + Circuit Breaker : Resilience4j
API Gateway + Config Server : Spring Cloud Config
API Gateway + Monitoring : Prometheus Grafana
API Gateway + Distributed Tracing : OpenTelemetry
API Gateway + Kafka
API Gateway + Kubernetes : NGINX Ingress, Spring Cloud Gateway

Difference Between Load Balancer and API Gateway?

API Gateway ≠ Load Balancer
API Gateway vs Reverse Proxy
API Gateway vs Service Mesh
API Gateway vs Reverse Proxy
API Gateway vs Service Discovery

# Routing

```
/api/users/** 
/api/orders/** 
/api/payments/**


/api/users/**     → User Service
/api/orders/**    → Order Service
/api/payments/**  → Payment Service

```


Should Authentication/Authorization at APIGateway or before Service ?
Why not put authentication inside every microservice?
What about downstream stream ?

Gateway authentication does not mean downstream services should blindly trust every request.
For sensitive operations, services can independently validate identity/authorization.

401 vs 403 Trap

# RateLimiting

Why Rate Limit at Gateway?

Rate Limiting Algorithm
1. Fixed Window
2. Sliding Winodw
3. Token Bucket
4. Leaky Bucket




