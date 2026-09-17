Architectural Style 
1. Monolithic : Rollback  
2. Microservice : 

ACID Vs BASE 

ACID : Use ACID within a single microservice where all operations are on the same database.
BASE : Use BASE between multiple microservices.

A → Atomicity 
C → Consistency 
I  → Isolation 
D → Durability

B A → Basically Available
S → Soft State
E → Eventual Consistency

How to Handle Distributed Transactions?
1. SAGA Pattern
	1. Choreography
	2. Orchestration
2. Eventual Consistency
3. Compensating Transactions
4. Transactional Outbox Pattern
5. Idempotency
6. Retry Mechanism
7. Avoid Distributed Locking
8. Usually Avoid 2 Phase Commit.
9. Usually Avoid 3 Phase Commit.

Phase Commit 
- 2PC
- 3PC

2 Phase Commit 
2PC
1. Prepare
2. Commit

https://www.youtube.com/watch?v=d2z78guUR4g
- Watch Video for 2 Phase Commit

3 Phase Commit

3PC
1. CanCommit
2. PreCommit
3. DoCommit

Are they really used or not ?  🤔🤔🤔 


SAGA 2PC Microservice Transaction
https://www.youtube.com/watch?v=d2z78guUR4g
2PC vs Orchestration Based

https://www.youtube.com/shorts/12r1zGPCbF8

2PC
- Real
- Still used in some controlled environments
- Usually avoided for loosely coupled microservices

3PC
- Real
- Mostly academic / specialized
- Rare in production


SAGA Design Patten
SAGA : Sequential Approach to General Availability

A SAGA breaks one large transaction into multiple smaller local transactions.

Types 
1. Choreography Saga 
	Events
	Compensating Transaction
2. Orchestration Saga 
	BPMN  : Business Process Model and Notation 	Graphical Way
	Camunda
	Central Coordinator
[]()
Transactional Outbox Pattern 
1. InBox
2. OutBox

Transactional InBox-Outbox Pattern https://www.youtube.com/watch?v=7Js-4GuNogM
[Transactional-Outbox-Pattern](obsidian://open?vault=studywithme_HLD&file=Excalidraw%2FOutbox-Inbox-Pattern.excalidraw)

---

```
                 DISTRIBUTED TRANSACTION
                         │
             ┌───────────┴───────────┐
             │                       │
        Saga Pattern                2PC
             │                       │
       Eventual Consistency      Strong Atomicity
             │
       Compensating Actions
             │
     ┌───────┴────────┐
     │                │
Outbox            Idempotency
     │                │
Reliable Events    Safe Retries
```