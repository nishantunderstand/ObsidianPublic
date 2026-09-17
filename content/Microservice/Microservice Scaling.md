Architectural Style 
1. Monolithic
2. Microservice

Scaling
1. Vertical Scaling (Scale Up)
2. Horizontal Scaling (Scale Out)

Parameter of Judgement : 
1. CPU 
2. Memory
3. Throughout
4. Latency
5. Concurrency
6. Stateless  : Horizontal
7. Traffic Growth : Hardware Limitation
8. Availability
9. Cost 


Manual Scaling vs Auto Scaling
Auto Scaling Group

How to decide whether to go for Horizontal or Vertical ?

```
                 Traffic / Load increasing?
                          │
                         YES
                          │
                 What is the bottleneck?
                    ┌─────┴─────┐
                    │           │
              CPU / Memory    I/O / Concurrency
                    │           │
                    ▼           ▼
             Can one machine   Need more
             handle growth?    instances?
                │                  │
             YES │                  │ YES
                ▼                  ▼
          Vertical Scaling    Horizontal Scaling
```

Judgments
1. Small/simple application
2. Traffic is unpredictable/growing
3. Availability is important
4. Statelessness is a major factor
