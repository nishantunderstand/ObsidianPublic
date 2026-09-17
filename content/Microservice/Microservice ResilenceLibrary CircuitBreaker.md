Circuit Breaker States
1. Closed
2. Open 
3. Half Open 

---

AOP + Exception (Checked / Unchecked Exception)

Fallback Method 
1. Same Class
2. Different Class

AOP Concept
Self Invocation Problem

---
Is Fallback mandatory ?
Can I have multiple fallback methods?
Can fallback itself throw an exception?
Fallback Method Signature relation with original Method 
Can fallback have a different return type?
What if the original method has parameters?


---

Can Circuit Breaker Recover Automatically ? 
If fallback returns successfully, will the Circuit Breaker become CLOSED?
If Circuit Opens, What User Gets?
Can We Use All Together?

---

Does fallback mean retry?
Does Circuit Breaker Fix the Downstream Service?
Does Circuit Breaker Fix Down Service?

CircuitBreaker with Exponential TimeOfff

  
[https://medium.com/%40shivanimutke2501/day-43-system-design-concept-circuit-breaker-6063b3b754a6](https://medium.com/%40shivanimutke2501/day-43-system-design-concept-circuit-breaker-6063b3b754a6)


---
Resilience4j SpringBoot

```java
@CircuitBreaker(name="PaymentService", fallbackMethod="fallback")
public String callPaymentService(){
	return restTemplate.getForObject("http://payment/api",String.class);
}

public String fallback(Exception ex){
	return "Payment Service Unavailable";
}
```


Dependency name Maven One 👈👈👈👈👈

Spring Boot Tool Name? resilience4j-spring-boot3
How to enable in SpringBoot ?
