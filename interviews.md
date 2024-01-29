# System Design Interviews
(Notes taken from System Design Course by Karan)
- These are designed to eveluate my capability to produce technical solutions to abstract problems, thus not designed for a specific answer.
- designed with different expectations for different engineering levels
## Common Strategies.
### Requirement clarifications
- systemd design questions ar vague or abstarct by nature.
- Asking questions about the exact scope of the problem, and clarifying functional requirements early in the interview is essential. requirements are divided into the following categories
#### Functional Requirements
these are the requirements that the end user specifically demands as basic functionalities that the system should offer. all these functionalitites need to be necessarily incorporated into the system as part of the contract.
examples
- what are the features we need to define for this system
- what are the edge cases we need to consider if any in our design?

#### Non-Functional Requirements
these are the quality constraints that the system must satisfy according to the project contract. the priority or extent to which these factors are implemented varies from one project to another. they are also called non-behavioural requirements. for example
      - portability
      - maintainability
      - reliability
      - scalability
      - security

#### Extended Requirements
These are basically nice to have requirements that might be out of the scope of the system.
exanples
- our system should record metrics and analytics
- service health and performance monitoring

### Estimation and Constraints
Estimate the scale of the system we are going to design. it is imortant to ask questions such as
  - what is the desired scale this isystem will need to handle?
  - what is the read/write ratio of our system
  - how many requests per second
  - how much storage will be needed
these questions will help in later scaling the design

### Data Model Design
once we have the estimations, we can start with defining the database schema. Doing so in the early stages of our interview would help us to understand the data flow which is the core of every system. in this step, we basically define all the entities and relationships between them.
  - what are the different entities in the system
  - what are the relationships between the entities
  - how many tables do we need
  - is NoSql better here

  ### API Design
  Next we can strat designing APIs for the system. These APIs will help us define the expectations from the system explicitly. we dont have to write any code, just a simple interface defining the API requirements shuch as
        - parameters
        - functions
        - classes
        - types
        - enitites
for example

```java
  createUser(name: String, email: String): User
```

it is advised to keep the interface as simple as possible and come back to it later whn covering extended requirements.

### High Level Component Design
Now we have established our data model and API design, it is time to identify system components(such as load balancers, API Gateway, etc.) that are needed to solve our problem and draft design of our system.

  - is it best to design a monolithic or a microservices architecture?
  - what type of database should we use

once we have a bsic diagram, we can start discussing with the interviewer how the system will work from the client's perspective.

### Detailed Design
Now it is time to go into detail about the major components of the system we designed. as always, discuss with the interviewer which component may need further improvements.

Here is a good opportunity to demonstrate your experience in the areas of your expertise. Present different approaches, advantages, and disadvantages.
Explain your design, and back them up with examples. this is also a good time to discuss any addtional features the system might be able to support, though this is optional.
  - how should we partition our data
  - what about load distribution
  - should we cache
  - how will we handle sudden spike in traffic

try not to be too opinionated abot certain technologies, statements like "I believe tha NoSQL databases are just better, SQL databases are not scalable" reflect poorly.
 - Pro - tip -> be humble about what you know and what you do not. use your existing knowledge with examples to navigate this part of the interview.

 ### Identify bottlenecks and resolve them
 Finally, it is time to discuss bottlenecks and approaches to mitigate them. exmple of good questions are:
  - do we have enough database replicas
  - is there any single point of failure
  - is database sharding required
  - how can we make our system more robust
  - how to improve the availability of our cache

Make sure to read the engineering blog of the company you are intervuewing with. this will help you get a sense of what technology they are using and which problems are important to them