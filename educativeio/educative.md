# Introduction to Modern System Design
## What is system Design
**System Design** is the process of defining components and their integration, APIs, and data models to build large scale systems that meet a specified set of functional and non functional requirements.
system design uses the concepts of computer networking, parallel computing, and distributed systems to craft systems that scale well and are performant. Distributed systems scale well by nature. However, distributed systems are inherently complex. The discipline of system design helps us tame this complexity and get the work done. 
System design aims to build systems that are reliable, effective, and maintainable, among other characteristics

* **Reliable systems** handle faults, failures and errors
* **Effective Systems** meet all user needs and business requirements
* **maintainable systems** are flexible and easy to scale up or down. The ability to add new features also comes under the umbrella of maintainability

## Modern system design using building blocks
we have separated out commonly-used elements, such as load balancers, as the building blocks for higher-level system design. this serves tow purposes. First it allows us to discuss all the building blocks in detail and discuss their interesting mini design probllems. Second, when we tackle a design problem, we can concentrate on problem specific aspects, mention the buildng block we will use and how we will use. This helps us remove duplicate discussions of commonly occuring design elements. 

we have identified sixteen building blocks that are crucial in designing modern systems.
![Screenshot 2024-02-26 at 14.11.45.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_KHnSC3%2FScreenshot%202024-02-26%20at%2014.11.45.png)

## About this Course
this course is about designing systems that scale with increasing users, remain available even under different faults, and meet functional goals with good performance. Real-world system building is an iterative process where we start with a reasonably good design, measure how it performs, and improve the design in the next iteration.
The focus of this course is to immerse ourselves into carefully-selected system design endeavours to enable ourselves to tackle any novel design problem, be it in a system desin interview or a task at the office. this course aims to teach concepts instead of giving out boilerplate designs. Some gaps that thos course aims to filter are listed below

**A fresh look at system design**: many system design courses provide a formula to attack a specific problem. this might seem attractive in a a high stress situation like an interview, but it might encourage memorizing a design solution instead of actually understanding the problem and devising an appropriate solution. if system design were that formulatic, then we probably would not need people for system designing. system design is as much an art as it is a science., and attacking a design problem from the first principles give a fresh feel to it.
**Going deep and broad**: we tackle some traditional problems, but with added in depth discussions in them. we give proper rationale for why we use some components despite their tradeoffs. for example, we explain why we use a particular database , a caching system , or a load balancing technique in a design. 
we address some new design problems as well that touch upon not only scalability but also availability, maintainability, consistency, and fault tolerance. Collectively, traditional and new problems cover all aspects of modern system design activity. our hope is that this course prepares learners to effectively tackle any new design problem they encounter.
new systems are complex, and often, we might need to make appropriate assumptions to properly scope a problem. we cover problems in more detail to properly grasp the real-world systems.
**Iterative Process**: Systems, in reality, improve our iterations. we often start with something simple but when bottlenecks arise in one or more of the systeams parts, a new design becaomes necessary. in some design problems, we make one design, identify bottlenecks, and improve on it. working under the constarints might not permit iterations on the design . However we still recommend two iterations- first, where we do our best to come up with a design(that takes about 80 percent of or time) and a second iteration for improvements. another choice is to change things as we figure out new insights. Inevtiably we discover new details as we spend more time working with a problem. 
**Interactive Learning**: we provide ample opprtunities to get experience with system design. some design problems guide learners through many steps to design a system. we also have a few examples where the learner designs the full system end-to-end without any guided steps. we reinforce the important concepts by testing learners with questions and quizzes. 

## Who should take this course
System design is for any software engineer who wants to advance in their career.
**Interview preparation**: Lately, system design is becoming an important part of software development interviews. this course elps software engineers prepare for interviews . we have an elaborate guide on preparation for a system design interview i the second chapter of this course for learners who are interested. 
**Software developers**: System design is primarily for back-end developers who aim to become principla engineers or solution architects. it is because these engineers handle actual user data. once the data is submitted to backend systems by the front-end, effective handling of data makes the overall application successful. Having said that, full stack or fronend developers may also want to learn system design to improve their work. at the same time, support engineers who work on-call in the production environment have to dal with all sorts of problems daily. therefore, system design concepts enable SREs to efficiently find the root cause of complex problems. 
**Product / Project managers**: a big challenge in product/projec amanagement is to build systems that scale well and perform effectively over time. managers that are aware of system design can steer the design of large scale performant systems. therefore, it is imperative for product/project managers to understand system design concepts to lead the design and development of successsful applications
**System Design Learners**: system design is an interesting subject, and people in tech domains can greatly benefit rom learning system design. This course helps a learner understand how giant tech companies design and build successful applications from scratch and improve them over time. other learners may want to develop their idea into a large application by learning from this course. 

## Prerequisites for this course
we assume that you know the fundamental concepts of a distributed system. 

## Course Structure

this course consists of forty chapters. these chapters can be segmented inot four different sections.
1. **Introduction**: This section is composed of five chapters. the first chapter introduces the course and its key features. the second chapter guides how to prepare for the system design interview. The third chapter talsk about different types of abstractions.Next we discuss some indesipensable non-functional characteristics that every large-scale system should have. We wrap this chapter up with back-of the ennvlope calculations that enable us to estimate resources during ur design problems.
2. **Building Blocks**: the building blocks chapter starts with an introductory lesson presentin sixteen different building blocks. Each of these blocks is explained in an independent chater. we conclude this sectionm with the conclusion chapter which also serves as an introduction to the next section
3. **Design Problems**: This section is the meat of the course and is carefully crafted from thirteen design problems. 
4. **Epilogue**: here, we wrap up this course and is made up of three chapters. Te first covers spectacular failures that show how, in the real world, even a small mistakle can bring down a large and successfu application . such failures may be inevitable but we highlight some measures to mitigate such failures. we conclude the course with the concluding remarks chapter.
![Screenshot 2024-02-26 at 14.52.14.png](..%2F..%2F..%2FScreenshot%202024-02-26%20at%2014.52.14.png)

### Strengths of the course
while filling some important gaps in other available courses, we believe this course has some key strengths to offer. we summarize the strengths and advanages this course has over others in the table given below.

| Strengths                                             | Advantage                                                                                                                 |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Building Blocks                                       | This is a modern approach to system design where we construct bigger artifacts using smaller building blocks              |
| Building blocks as design problems                    | we will treat each one of our building blocks as a stan-alone mini design problem                                         |
| incremental improvement to design                     | layer-by-layer design solution addresses added bottlenecks, designing simple and incremental solutions to complex systems |
| evaluating the design                                 | accountability of the provided design solution shows the performance of our design                                         |
| solving the traditional problems with updated designs | this course is up to date with the latest industry demands                                                                |
| new design problems added                             | this course contains updates to decades-old system design courses                                                         |
| careful collection of design problems                 | each problem has its own unique aspects in terms of problem-solving and designing                                         |
| contribution by experts from FAANG                    | learn from the best                                                                                                       |
| AI-based quizzes and assessments                      | these assessments and interviews evaluate learners concepts of system design                                              |

Let us dive right in. 


# What is a system design interview?
This course is equally useful for people already working and those preparing for interviews. In this chapter, we highlight the different aspects of a system deaign interview(SDI) and some helpful tips for those who are preparing for an upcoming interview. we encourage learners to read this chaoter even if they are not preparing for an interview because some of the topics covered n this chapter can be applied broadly. 

## How are SDIs different from other interviews.
just like with any other interview, we need to approach the system design interviews strategically . SDIs are different from coding interviews. There is rarely any coding required in this interview. 
an SDI takes place at a much higher level of abstraction. we figure out the requirements and map them on to the computational components and the high-level communication protocols that connect theses subsystems .

the final answer doe not matter what matters is the process and the journey that a good applicant takes the interviewer through.
**As compared to coding problems i interviews, system design is more aligned with the tasks we will complete on our jobs**

## How do we tackle a design question?
Design questions are open ended, and they are intentionally vague to start with. such vagueness mimics the reality of modeern day business. 
Interviewers often ask about  well-knon problem - for example designing whatsapp. Now a real whatsapp application has numerous features and including all of them as requirements for our Whatsapp clone might not ne a wise idea due to the following reasons. 
* First, we will have limited time during the interview
* Second, working with some core functionalities of the system should be enough to exhibit our problem solving skills
we can tell the interviewer that there are many other things that a real whatsapp does that we don't intend to include in our design. if the interviewer has any objections we can change our plan of action accordingly. 
* Here are some best pracices that we should follow during a system design interview.
![Screenshot 2024-02-26 at 15.28.20.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_8RtO5X%2FScreenshot%202024-02-26%20at%2015.28.20.png)

* An applicant should ask the right questions to solidify the requirements
* applicants also need to scope the problem so that they are able to make a good attempt at solving it within the limited time frame of the interview. SDIs are usually about 35 to 40 minutes long.
* Communication with the interviewer is critical. it is not a good idea to silently work on the design  Instead we should engage with the interviewer to ensure that they understand our thought process
## Present the high level design
At a high level, components could be frontend , load balancers, caches, data processing, and so on. The system design tells us how these components fit together. 
An architectural design often represnents components as boxes. the arrows between these boxs represent who talks to whom and how the boxes or components fit together collectively
![Screenshot 2024-02-26 at 15.56.44.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_GxTfA5%2FScreenshot%202024-02-26%20at%2015.56.44.png)
we can draw a digram like the one shown above for the given problem and present it to the interviewer.

## Possible questions for every SDI
SDIs often include questions related to how a design might evolve over time as some aspect of the system increases by some order of magnitude - for example, the number of users, the number of queries per second, and so on. It is commonly believed in the systems community that when some aspect of the system increases by a factor of ten or more, the same design might not hold and might require a change. 
Designing and operating a bigger systeem requires careful thinking because designs often dont linearly scale with increasing demands on the system. 
Another question in an SDI might be related to why we dont design a system that is already capable of handling more work than necessary or predicted. 
**The dollar cost associated with complex projects is a major reason why we dont do that**

## The design evolution of Google
The design of the early version of google Search may seem simplistic  today, but it was quite sophisticated for its time. it also kept costs down, which was necessary for a startuplike gOOGLE TO STAY AFLOAT. tHE UPSHOT IS THAT WHATEVER WE DO AS DESIGNORS HAVE IMPLICATIONS FOR THE BUSINESS AND ITS CUSTOMERS. WE NEED TO MEET OR EXCEED CUSTOMER NEEDS BY EFFICIENTLY UTILIZING RESOURCES.

## Design Challenges
Things will change and things will break over time because of the following.
* there is no single correct approach or solution to a design problem. 
* A lot is predicated on the assumptions we make
## The responsibility of the designer
As designers we need to provide fault tolerance at the design level because almost all modern systems us off-the-shelf components, and there are millions of search components. so something will always be breaking down, and we need to hide this undesirable reality from our customers.

## Who gets a system design interview
Traditionally, mid-to-deior level candidates with more than two years of experience get at lease one system design interview. for more senior applicants, two or thress system design interviews are common. 
Recently, large companies have also put forth system design questions to some junior candidates. It is never too early to learn system design to grow or even expedite careers.
## Theory and practice
Most of the theory of system design comes from the domain of distributed systems. Getting a refresher on these concepts is highly recommended. 
Distributed systems give us guideposts for mature software principles. These include the following
* Robustness(the ability to maintain operations during a crisis)
* Scalability
* Availability
* Performance
* Extensibility
* Resiliency(the ability to return to normal operations over an acceptable period of time post disruption)
Such terminologies also act as lingua franca between the interviewer and the candidate
as an example we might say we need to make a trade-off between availability and consistency when network components fail because the CAP theorem indicates that we cant have both under network partitions. such common language helps with communication and shows that we are well versed in both theory and practice.
* **Note:** it is a candidate's job to exhibit their skills to the interviewer.

## How to prepare for success
- substantial preparation is necessary to increase our odds of getting the job we apply for.
- depending on a candidate's seniority and proficiency, different candidates need different times for interview preparation,. 
- for an average candidate, three to four months might be required to prepare for a syste design interview. 
## This course
- this course helps learners learn or brush up on their system design skills. we have carefully curated some traditional and fresh design problems to cover the substantial depth and breadth of the system design.
- the following activities might expedite the preparation and add variety and further depth to a candidates knowledge.
### Technical blogs
- many companies regularly publish the technical details of their significant work in the form of technical blogs. why are companies eager to share the technical details of their work?
  - the reason for such sharing is to excite the technical community about the fact that the company is solving hard problems. they also hope to motivate more people to join the company.
  - such blogs can also help to advertise company products to b2b customers
  - Additionally, such materials help the company train potential future workers on their own time.
- There is a fine line between what can be held back by a company due to a competitive edge and what can be made public
we can study these blogs to get insight into what challenges or problems the company faced and what changes they made in the design to cope with these challenges.
**Note:** Staying informed about these innovations is important for professionals , and it is even more crucial for an applicant.
- 

## Ask why a system works
By asking themselves the right questions, candidates can think through dense and ambiguous situations
* lEARN HOW POPULAR APPLICATIONS WORK AT A HIGH LEVEL - FOR EXAMPLE tWITTER, instagram, AND SO ON.
* Start to understand and ask why some component was used instead of another e.g Firebase vs SQL
* build serious side projects. Start with a simple product and then improve and refine it.
* build a system from scratch, and get familiar with all the processes and details of its construction.
- we can clone a popular application without a tutorial

## The right direction
System design deals with components at a higher level, and we need to avoid going to the trenches
**we should concentrate less on mechanics and more on tradeoffs**

for example, discussing whether to use Room library instead of raw SQLite is not helpful because Room library is a mere wrapper around SQLite. a better discussion might be about using traditional databases like mysql or using nosql stores like mongoDB. this second discussion will help pinpoint trade-offs between the two. 
we should start with high level stuff because the low-level details will automatically come up. 

## Mock interviews
**mock interviews** are a great way to prepare for system design interviews. they involve pairing up with a friend and allowing them to ask questions. if it is not possible to use a friend, another strategy is to record ourselves and play the role of both interviewer and interviewee. with this approach we can critique ourselves or ask a knowledgeable friend for feedback. 
**Note**: Since no mock interview can fully mimic an actual interview, it is good idea to take real interviews in companies. Once we have been through an interview or two, we will be better able to evaluate what went right and what did not.

## How to perform well
here are a few tips on how to perform well during a SDI

### What to do during the interview
we stress that a candidate should make an effort to avoid looking unoriginal. The interviewer has probably asked the same question to many candidates. Reproducing a run-of-the-mill design might not impress the interviewer.
at the same time, an interview can be stressful situation. Having a plan to attack the problem might be a good strategy. Depending on the candidate, there can be multipke startegies to attack a design problem. we suggest the following technique. 
### Strategize, then divide and conquer
we recommend including the following activities somewhere in the interview

ASK REFINING QUESTIONS -> HANDLE DATA -> DISCUSS THE COMPONENTS -> DISCUSS TRADE-OFFS

## ASK REFINING QUESTIONS
- we need to understand the design problem and its requirements. To do this, we can put our product manager hat and prioritize the main features by asking the interviewer refining questions. the idea is to go on a ourney with the interviewer about why our design is good. these interviews are designed to gauge if we are able to logically derive a system out of vague requirements,
- we should ensure that we are solving the right problem. often, it helps to divide the requirements into two groups
* Requirements that the clients need directly for example, the ability to send messages in near real-time to firends
* Requirements that are needed indirectly for example, messaging service performance should not degrade with increasing user load.
**Note**: professionals call these functional and nonfunctional requirements

## HANDLE DATA
- we need to identify and understand data and its characteristics in order to look for appropriate data storage systems and data processing components for the system design.
- some important questions to ask ourselves when searching for the right systems and components include the following
* what is the size of the data right now?
* at what rate is the data expected to grow over time?
* how will the data be consumed by other subsystems or the end users?
* is the data read or write heavy?
* do we need strict consistency of data, or will eventual consistency work?
* what is the durability target of the data?
* what privacy and regulatory requirements do we require for storing or transmitting user data?

## DISCUSS THE COMPONENTS
- at some level, our jo might be perceived as figuring out which components we will use , where they will be placed and how they will interact with each other
- an example could be the type of database - will a conventional database work, or should we us a NoSQL database?
- there might be cases where we have strong arguments to use NoSQL databases, but our interviewer may insist that we use a traditional database. what should we do in such a case
  - As designers, we'd have a harder job because we'd need to use a traditional database and no extra work to ameliorate the shortcomings or challenges. In this case, we'd have invented a new component. such interactions during interviews are also excellent opportunities to exhibit ur design skills. 
- **Note:** we often abstract away the details of the components as boxes and use arrows to show the interactions between them. it might help to define the user-facing APIs at a high level to further understand system data and interaction requirements. 
- frontend components, load balancers, caches, databases, firewalls, and CDNs are just some examples of system components.

## DISCUSS TRADE-OFFS
- Remember that there is no one correct answer to a design problem. if we give the same problem to two different groups, they might come up with different designs. 
- these are some of the reasons why such diversity exist in design solutions
* Different components have different pros and cons. we will need to carefully weigh what works for us. 
* different choices have different costs in terms of money and technical complexity. we need to efficiently utilize our resources
* every design has its weaknesses. as designers, we should be aware of all of them, and we should have a follow up plan to tackle them
we should point out weaknesses in our design to our interviewer and explain why we haven't tacled them yet. an example could be that our current design cannot handle ten times more load, but we don't expect our system to reach that level any time soon. we have a monitoring system to keep a very close eye on load growth over times so that a new design can be implemented in time. this is an example where we intentionally had a weakness to reduce system cost. 
* something is alwasy failing in a big system. we need to integrate fault tolerance and security into our design. 

## What not to do in an interview
Here are a few things that we should avoid doing in an SDI

* dont write code
* dont start building without a plan
* dont work in silence
* dont describe numbers without reason, we have to frame it
* if we dont know something, we dont paper over it, and we dont pretend to know it.
**Note:** if an interviewer asks us to design a system we have not heard of, we should just be honest and tell them so. the interviewer will either explain it to us or they might change the question.


# Abstractions and their importance
**Abstraction** is the art of obfuscating details that we dont need. it allows us to concentrate on the big picture. looking for the big picture is vital because it hides the inner complexities, thus giving us a broader understanding of our set goals and staying focused on them.
- in the context of computer science, we all use computers for our work, but we dont start making hardware from scratch and developing an operating system. we use that for the purpose at hand rather than digging into building the system
- the developers use a lot of libraries to develop the big systems. if they start building the libraries, they wonnt finish their work. Libraries give us an easy interface to use functions and hide the inside detail of how they are implemented. a good abstraction allow us to reuse it in multiple projects with similar needs.
## Database abstraction
**Transactions** is a database abstraction that hides many problematic outcomes when concurrent users are reading, writing or mutating the data and gives a simple interface of commit, in case of success or abort in case of failure. either way, the data moves from one consistent state to a new consistent state. the transaction enables end users to not be bogged down by the subtle corner-cases of concurrent data mutation, but rather concentrate on their busines logic.

## Abstractions in distributed systems
Abstractions in distributed systems help engineers simplify their work and relieve them of the burden of dealing with the underlying complexity of the distributed systems.

the abstraction of distributed systems has grown in popularity as many big companies like Amazon AWS, Google C;loud, and microsft azure provide distributed services. every service offers different levels of abstraction. the details behind implementing these distributed services are hidden from the users, thereby allowing the developer to focus on the application rather than going into the depth of the distributed systems that are often very complex.
today's applications cant remain responsive/functional if they are based on a single node because of an exponentially growing number of users abstractions in distributed systems help engineers shift to distributed systems quickly to scale their applications.
**Note:** we will see the use of abstractions in communications, data consistency, and failures in this chapter. the purpose is to convey the core ideas, but not nnecessarily all the subtleities of the concepts

## Remote Procedure calls
**Remote Procedure calls(RPCs)** provide an abstraction of a local procedure call to the developers by hiding the complexities of packing and sending function arguments to the remote server, receiving the retun values, and managing any network tries. 
### What is an RPC
**RPC** is an interprocess communictaion protocol that is widely used in distributed systems. in the OSI model of network communication, RPC spans the transport and application layers. 
RPC mechanisms are employed when a computer program causes a proceudre or subroutine to execute in a separate address plcae
**Note:** the procedure or subroutine is coded as a regular /local procedure call without the programmer explicitly coding the details of the remote interaction

### How does it work?
when we make remote procedure call, the calling environment is paused and the procedure parameters are sent over the network to the environment where the procedure is to be executed.
when the procedure execution finishes, the results are returned to the calling environment where execution restarts as a regular procedure call. 
to see how it works ,let us take an example of a client-server program. there are five main components involved in the rps program, as shown below

![Screenshot 2024-02-27 at 12.18.03.png](..%2F..%2F..%2FScreenshot%202024-02-27%20at%2012.18.03.png)

- the client, the client stub and one instance of RPC runtime are running on the client machine. the server , the server stub and one instance of RPC runtime are running on the server machine
- during RPC process, the following steps occur
1. a client initiates a client stub process by giving parameters as normal. the client stub is stored in the address space of the client
2. the client stub converts the parameters into a standardized format and packs them into a message. after packing the parameter into a message , the client stub requests the local rpc runtime to deliver the message to the server.
3. the rpc runtime at the client delivers the message to the server over the network . after sending a message to the server, it waits for the message result from the server.
4. rpc runtime at the server receives the message and passes it to the server stub
**Note**: the RPC runtime is responsible for transmitting messages between client and server via the network. the responsibilities of rpcruntime also include retransmission, acknowledgement, and encryption
5. the server stub unpacks the message, takes the parameters out ot it, and calls the desired server routine, using a local procedure call, to do the required execution. 

![Screenshot 2024-02-27 at 12.25.30.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_WldMRu%2FScreenshot%202024-02-27%20at%2012.25.30.png)
6. after the server routoine has been executed with the given parameters, the result is retuned to the server stub. 
7. the server stub packs the returned result into a message and sends it to the RPC untime at the server on the transport layer.
8. the server's rpc runtime that was waiting for the result  now receives the result and sends it to the client stub.
9. the client stub unpacks the result, and the execution process returns to the caller at this point. 
**Note:** Back-end services use RPC as a communication mechanism of choice due to its high performance and simple abstraction of calling remote code as local functions.

### Real-world usage
RPCs are used in many real-world services. take a look at the exemples elow

* **Google**: Google uses rpcs in various parts of its distributed infrastructure. they have developed gPRC, an open source framework that uses RPC to build efficient and highly performant distributed systems. it is employed for services like google search, youtube e.t.c. where it allows google to maintain communication and data exchange between different components of their services, whcich is essential for achieving real-time performance.
* **Uber**: uber uses RPC for various functions, including real-time location tracking, ride mathcing, and communication between frivers and riders. RPC allows Uber to provide fast and responsive services by facilitating data exchange between the users's app and the server
* **Facebook:** most services at facebook are written using Thrift for RPC, and some storage systems use Thrift for serializing records on disk. This provides several benefits to Facebook. for example, it enables interoperability between different languages such as Python client communicating with a c++ server

## Summary
the RPC method is similar to caling a local procedure, except that the called procedure is usually executed in a different process and on a different computer.
RPC allows developers to build applications on top of distributed systems. Developers can use the RPC method without knowing the network communication details. As a result they can concentrate on the design aspects, rather than the machine and communication-level specifics. 

## Spectrum of consistency models
### What is is consistency
in distributed systems, consistency may mean many things. one is that each replica node has the same view of data ata a given point in time. the other is that each read request gets the value of the recent write. these are not the only definitions of cnsistency, since there are many forms of cosistency. Normally, **consistency models** provide us with abstarctions to reason about the correctness of a distributed system doing concurrent data reads , writes and mutations
if we have to design or build an application in which we need a third party storage system like s3 or cassandra, we can llok into the consistency guarantees provided by s3 to decide whether to use it or not. let us explore differnet types of consistency

the two ends of consistency spectrums are
* strongets consistency
* weakest consistency.
there are consistency models that lie between these two ends, some of which are shown in the following illustration.
![Screenshot 2024-02-27 at 12.43.31.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_cyGIdc%2FScreenshot%202024-02-27%20at%2012.43.31.png)

There is difference between consistency in ACID properties and consistency in the CAP THEOREM
Database rules are at the heart of **ACID consistency**. if a schema specifies that a value must be unique, a consistent system will ensure that the value is unique throughout all actions. if a r=foreign key indicates that deleting one row will also delte associated rows, aconsistent system ensures that the sates can't contain related rows once the base row has been destroyed.

**CAP consistency** guarantees that in a distributed system, every replica of the same logical values has the same precise value at all times. it is worth noting that this is a logical rather than a physical guarantee. Due to speed of light, replicating numbers throughout a cluser may take some time. by preventing clients from accessing different values at separate nodes, the cluster can nevertheless give a logical picture. 

## Eventual consistency
**Eventual consistency** is the weakest consistency model. the applications that dont have strict ordering requirements and dont require reads to return the latest write choose this model. eventualconistency ensures all the replicas converge on a final value after a finite time and when no more writes are coming in. if new writes keep coming , replicas of an eventual consistent system might never reach same state. untill the replicas converge, diferent replicas can return different values. 
eventual consistency ensures high availability.
**example**
  the **domain name system** is a highly available system that enables name lookups to a hundred milliom devices across the internet. it uses an eventual consistency model and doesnt necessarily reflect the latest values.
**Note:** Cassandra is a highl available NoSQL database that provides eventual consistency.

## Causal consistency

**Causal consistency** works by categorizing operations into dependant and independent operations. **dependent operations** are also called causally-related operations. causal consistency preserves the order of the causally-related operations.

![Screenshot 2024-02-27 at 13.11.07.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Q8i7Lt%2FScreenshot%202024-02-27%20at%2013.11.07.png)

This model doesnt ensure ordering for the operations that are not causally related. these operations can be seen in different possible orders
causal consistency is weaker overall but stronger than the eventual consistency model. it is used to prevent non-intuitive behaviors.
**example**
the causal consistency model is used in a commenting system. for example, for the replies to a comment on a facebook post, we want to display comments after the comment it replies to. this is because there is a cause-and-effect relationship between a comment and its replies

**Note**: There are many consistency models other than the four discussed in this lesson, and there is still room for new consistency models. Researchers have developed new consistency models. for example wyatt lloyd proposed the causal+consistency model to speed up some specific types of trnasactions.

## Sequential Consistency
**Sequential Consistency** is stronger than the causal consistency model. it preserves the ordering specified by each client's program. However, sequential consistency doen't ensure that the writes are visble simultaneously or in the same order as they occured according to some global clock

**Example**
in social networking applications, we usually don't care about order in which some of our friends' post appear. however, we still anticipate a sngle friend's post to appear in the correct order in which they were created. similarly, we expect our friends' comments in a post to display in the order that they were submitted. the sequential consistency model captures all these qualities.

## Strict consistency aka linearizability
a **Strict consistency** or **linearizability** is the strongest consistency model. This model ensures that a read request from any replicas will get the latest write value. once the client receives the acknowledgement that the write operatio has been performed, other clients can read that value.
linearizability is challenging to achieve in a distributed system. some of the reasons for such challeneges are variable network delays and failures. the following slides show depicts how variable network delays make it possible for different parties to see differentvalues. 
![Screenshot 2024-02-27 at 13.26.27.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_vrrWCg%2FScreenshot%202024-02-27%20at%2013.26.27.png)

Usually, synchronous replication is one of the ingredients for achieving strong consistency, though it in itself is not sufficient. we might need consesus algorithms such as Paxos and Raft to achieve strong consistency
linearizability affects the system's availability which is why it is not always used. applications with strong consistency requirements use techniques like **quorum based replication** to increase the system's availability.

**example**
Updating an account's password requires strict consistency. for example, if we suspect suspicious activity on our bank account, we immediately change our password so that no unauthorized users can access our account . if it were possible to access our account using an old p[assword due to a lack of strict consistency, then changing passwords would be a useless security strategy. 
**Note**: Google's Spanner database claims to be linearizable for many of its operations. 

## Summary
- linearizable services appear to carry out transactions/operations in sequential, real-time order. They make it easier to create suitable applications on top of them by limiting the number of values that services can return to application process. 
- linearizable services have worse performance rates than services with weaker consistency in excghange for their strong assurances. Think about a read in a key-value store that returns the value written by a concurrent write . the read imposes no limits on future reads if the key-value store is weakly consistent. 
- Application programmers have to compromise performance and availability if they use services with strong consistency models. the models may break the invariants of applications built on top of them in exchange for increased perfromance.


## Spectrum of Failure models
Failures are obvious in the world of distributed systems and can appear in various ways. They might come and go, or persist for a long period of time.
failure models proide us a framework to reason about the impact of failures and possible ways to deal with them

Here is an illustration that presents a spectrum of different failure models
![Screenshot 2024-02-27 at 13.37.55.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_qSL3y4%2FScreenshot%202024-02-27%20at%2013.37.55.png)


### Fail-stop
in this type of failure, a node in the distributed system halts permanently. However, the other nodes can still detect that node by communicating with it. 
from the epspective of someone who builds distributed systems, fail-stop failures are the simplest and the most convinient

### Crash
in this type of failure, a node in the distributed system halts silently, and the other nodes cannot detect that one node has stopped working

### Omission failures
in **Omission failures**, the node fails to send or receive messages. There are two types of omisssion failures. if the node fails to respond to the incoming request , it is said to be a **send omission failure**. if the node fails to receive the request and thus can't acknowledge it, it is said to be a **receive omission failure**.
### Temporal Failures
in **Temporal Failures**, the node generates correct results but is too late to be useful. Tis failure could be due to bad algorithms, a bad design startegy or a loss of synchronization between the processor clocks

### Byzanite failures
in **Byzanite failures**, the node exhibits random behaviour like transmitting arbitrary messages at arbitrary times, producing wrong results, or stopping midway. This mostly happens due to an attack by a malicious entity of a software bug. A byzanite failure is the most challenging type of failure to deal with. 

# Non-functional System Characteristics

## Availability
**Availability** is the percentage of time that some service or infrastructure is accessible to clients and is operated upon under normal conditions. For example, if a service has 100% availability, it means that the said service functions and responds as intended all the time.

## Measuring availability
Mathematically, availability , A, is a ratio. The highe the A value the better. We can also write this up as a formula

      A(in percentage) = (Total time  - Amount of Time Service was down) / Total time * 100

we measure availability as a number of nines. The following table shows how much downtime is permitted when we are using a given number of nines

![Screenshot 2024-02-28 at 08.14.31.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_S5xK10%2FScreenshot%202024-02-28%20at%2008.14.31.png)

## Availability and service providers
Each service provider may start measuring availability at different points in time. Some cloud providers start measuring it when they first offer the service, while some measure it for specific clients when they start using the service. some providers might not reduce their reported availability numbers if their service was not down for all the clients. the planned downtimes are excluded. Downtime due to cyberattacks might not be incorporated into the calculation of availability. Therefore, we should carefully understand how specific provider calculates their availability numbers. 

## Reliability
**Reliability**, R, is the probability that the service will perform its functions for a specified time. R measures how the service performs under varying operating conditions.
we often use **mean time between failures (MTBF)** and **mean time to repair(MTTR)** as metrics to measure R

      MTBF = Total elapsed time - sum of downtime / total number of failures
      MTTR = total maintainance time / total number of repairs
we strive for a higher MTBF value and a low MTTR value

## Reliability and availability
Reliabilty and availability are two important metrics to measure compliance of service agreed-upon service level objectives
the measure of availability is driven by time loss, whereas the frequency and impact of failures drive the measure of reliability. Availability and reliability are essential because they enable the stakeholders to assess the health of the service. 

Relaiability and availability are two distinct concepts, but they are related. mathematically, A is a function of R. this means that the value of R can change independently , and the value of A dependes on R. therefore, it is possible to have situations hwere we have
  * low A , low R
  * low A, high R
  * high A, low R
  * high A, high R(desirable)

![Screenshot 2024-02-28 at 08.26.20.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_6skzcZ%2FScreenshot%202024-02-28%20at%2008.26.20.png)

**Note:** There are many variations of the MTFB metric, such as mean time to failure (MTTF). usually we use MTTF instead of mtbf for those cases where a failed component is replaced due to irreparable problems . a bad disk or a failed bulb are examples of irrepairable faults a replacement is required. 

**Reliability** measures how well a system performs its intended operations(functional requirements). 
**Availability** measures the percentage of time a system accepts requests and responds to clients. 

## Scalability
**Scalability** is the ability of a system to handle increasing amount of workload without compromising performance. a search engine for example must accomondate increasing numbers of users, as well as the amount of data it indexes.
the workload can be of different types, including the following
  * **request workload**: This is the number of requests served by the system
  * **Data/storage workload**: this is the amount of data stored by the system

## Dimensions
here, the different dimensions of scalability are
  * **size scalability**: A system is scalable in size if we can simply add additional users and resources to it.
  * **Administrative scalability**: this is the capacity for a growing number of organizations or users to share a single distributed system with ease
  * **geographical scalability**: This relates to how easily the program can cater to other regions while maintaining acceptable performance constaraints. in other words, the system can readily service a booad geographical resgion, as well as a small one

## Different approaches of scalability
### Vertical scalability - scaling up
refers to scaling by providing additional capabilities to an existing device eg CPUs or RAM. vertical scaling allows us to expand our present hardware or software capacity, but we can only grow it to the limitations of the server. the dollar cost of vertical scaling is usually high because we might need exotic components to scale up

### Horizontal scaling - scaling out
refers to increasing the number of machines in the network. we use commodity nodes for this purpose because of their attractive dollar-cost benefits. The catch here is that we need to build a system such that many nodes could collectively work as if we has a single, huge server. 
![Screenshot 2024-02-28 at 10.16.43.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_TmZ3zm%2FScreenshot%202024-02-28%20at%2010.16.43.png)

## Maintainability
besides building a system, one of the main tasks afteward is keeping the system up and running by finding and fixing bugs , adding new functionalities, keeping the system's platform upfated, and ensuring smooth system operations. one of the salient features to define such requirements of an exemplary system design is maintainability. we can further divide the concept of maintainability into three underlying aspects:
1. **operability**: this is the ease with which one can ensure the system's smooth operational running under normal circumstances and achieve normal conditions under a fault.
2. **lucidity**: this refers to the simplicity of the code. The simpler the code base, the easier it is to understand and maintain it, and vice versa
3. **modifiability**: this is the capability of the system to integrate modified, new, and unforeseen features without any hassle

## Measuring Maintainability
**Maintainability, M** is the probability that the service will restore its functions within a specified time of fault occurrence. M measures how conviniently and swiftly the service regains its normal operating conditions.
for example, suppose a component has a defined maintainability of 95% for half an hour. in that case the probability of restoring the component to its fully active form in half an hour is 0.95
**Note: Maintainability gives us insight into the system's capability to undergo repairs and modifications while it is operational**
we use **mean time to repair** as the metric to meausre M

      MTTR = total maintanance time / total number of repairs

in other words, MTTR is the average time required to repair and restore a failed component. Our goal is to have as low a value of MTTR as possible

## Maintainability and Reliability
Maintainability can be defined more clearly in close relation to reliability. The only differency betwen them is the variable of interest. Maintainability refers to ```tme-to-repair```, whereas relaibility refers to both ```time-to-repair``` and the ```time-to-failure```. combining Maintainability and reliabilit analysis can help us achieve availability, downtime and uptime insights

## Fault tolerance
Real-world, large scale applications run hundreds of servers and databases to accomondate billions of user's requests and store significant data. These applications need a mechanism that helps with data safety and eschews the recalculation of computationally intensive tasks by avoiding a single point of failure
**Fault tolerance** refers to a system's ability to execute persistently even if one or more of its components fail. here, components can be software or hardware. conceiving a system that is hundred percent Fault tolerant is practically very difficult.

let's discuss some important features for which Fault tolerance becomes a necessity.
availability focuses on receiving every client's request and by being accessible 24/7
reliability is concerned with responding by taking specified action on every client's request.

## Fault tolerance techniques
failure occurs at the hardware or software level, which eventaully affects the data. Fault tolerance can be achieved by many approaches, considering the system structure. 

### Replication
one of the most widel-used techniques is **replication-based Fault tolerance**. eith this technique, we can replicate both services and data. we can swap out failed nodes with healthy ones and a failed data store with its replica. A large service can transparently make the switch without impacting the end customers
we create multiple copies of our data in separate storage. All copies need to update regularly for consistency when any update occurs in the data. updating data in replicas is a challneging job. When a system needs storing consistency, we can synchronously update data in replicas. However, this reduces the availability of the system. we can also asynchronously update data in replicas when we can tolerate eventual consistency, resulting in stale reads untill all replicas conerge. thus, there is a trade-off between both consistency approaches. we compormise wither on availability or on consistency under failyres - a reality that is oulined in the CAP Theorem
![Screenshot 2024-02-28 at 10.39.55.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_tOPk8G%2FScreenshot%202024-02-28%20at%2010.39.55.png)

### Checkpoint
**checkpointing** is a technique that saves the system's state in stable storage for later retrieval in case of failure due to erors or service disruption. checkpointing is a Fault tolerance technique performed in many stages at different time intervals. when a distributed system fails, we can get the last computed data from the previous checkpoint and start working from there.
checkpointing is performed for diferent individual processes in a system in such a way that they represent a global state of the actual execution. depending on the state, we can divide checkpointing into two types

* **consistent state**: A state is consistent in which all the indivdual processes of a system have a consistent view of the shared state or sequence of events that have occured in a system. snapshots taken in consistent states have data in coherent states, representing a possible situation of the system . for a checkpoint to be consistent , typically the following criteria are met.
  * all updates to data that were completed before the checkpoint are saved. any updates to data that were in progress are rolled back as if they didn't initiate.
  * checkpoints include all the messages that have been sent or received up untill that checkpoint. No messages are in transit to avoid cases of missing messages.
  * Relationships and dependencies between system components and their states match what would be expected during normal operation. 
* **inconsistent state**: This is a state where there are discrepancies in the saved satte of different processes of a system. in other words, the checkpoints across different processes are not coherent and coordinated.

let's look at an example to understand consistent and inconsistent states in a better way. consider three processes represented by i, j, and k. Two messages m1, and m2 are exchanged between the prcesses. other than that, we have one snapshot/checkpoint saved for each process represented by C1i, C1j and c1k where 1 represents the number of snapshots for a process and the lowercase letter represents the process itself. 

![Screenshot 2024-02-28 at 12.16.39.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_YSIscA%2FScreenshot%202024-02-28%20at%2012.16.39.png)
in the illustration on the left, the first checkpoints at processes j and i are consistent brcause m1 is sent and received after the checkpoints. on the contrary, in the right-hand illustration the first chekpoint at process j doesnt know about m1 while the first checkpoint at process i recorded the reception of message m1. therefore it is an inconsistent state. 
the left hand illustration respresents state also because no communication is being performed among the processes when the system performs checkpointing. on the right hand side, we can see that the processes communicate through messages when the system performs checkpointing. 

# Back-of-the-envelope calculations

## Put  Back-of-the-envelope numbers in perspective
here we will learn how to use appropriate numbers in  Back-of-the-envelope calculations

## why do we use  Back-of-the-envelope calculations

A distributed system has compute nodes connected via a network. There is a wide variety of available comute nodes and they can be connected in many different ways.  Back-of-the-envelope calculations help us ignore the nitty-gritty details of the system (at least at the design level) and focus on more important aspects
some examples of  Back-of-the-envelope calculations could be 
* The number of concurrent TCP connections a server can support. 
* The number of requests per second a web, database, or cache server can handle
* the storage requirements
choosing an unreasonable number for such calculations can lead to a flowed design. Since we need good estimations in many design problems, we will discuss all the relevant concepts in details in this lesson.
these concepts include
  * the types of data center servers
  * the realistic access latencies of different components
  * the estimation of RPS that a server can handle
  * examples of bandwidth, servers, and storage estimation

## types of data center servers
**Data centers** dont have a single type of server. enterprise solutions use commdity hardware to save cost and develop scalable solutions. Below, we discuss the types of servers that are commonly used within a data center to handle different workloads. 
![Screenshot 2024-02-28 at 12.41.37.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_2jJiRs%2FScreenshot%202024-02-28%20at%2012.41.37.png)

### web servers
for scalability, the web servers are decoupled from the application servers. **web servers** are the first point of contact after load balancers. Data centres have racks full of web servers that usually handle apI calls from the clients. Depending on the service that is offered, the memory and storage resources in web servers can be small to medium. However, such servers require good computational resources. for example, facebook has used a web server with 32 GB of RAM and of 500 gb of storage space ut for its high end computational needs, it partnered with intel to build a custom 16-core processor. 
**Note: many numbers quoted are obtained from the data center design tha facebook open-sourced in 2011. due to the slowing of Moore's law-induced performance circa 2004, the numbers are not stale.**

### application servers
**application servers** run the core application software and business logic. the difference between web and application servers is somewhat fuzzy. application servers primarily provide dynamic content, whereas web servers mostly serve static content to the client, which is mostly a web browser. 
they can require extensive computational and storage resources. storage resources can be volatile and non-volatile. Facebook has used application servers with a RAM of up to 256 GB and two types of storage - raditional rotating disks and flash - with a capacity of up to 6.5 TB

### Storage servers

with the explosive growth of internet users, the amount of data stored by giant services has multiplied. additionally, various types of data are now being stored in different storage units. for instance, Youtube uses the following datastores.
  1. **blob storage** for its encoded videos
  2. a **temporary processing queue storage** that can hold a few hundred hours of video content uploaded to youtube for processing
  3. specialized storage called **bigtable** for storing a large number of thumbnails of videos. 
  4. **Relational database management system** for users and videos metadata
other data stores are still used for analytics - for example, Hadoop's HDFS . storage servers mainly include structured and non-structured data management systems.

coming back to facebook, we know that they have used servers with a storage capacity of up to 120TB. with the number of servers in use, facebook is able to house exabytes of storage. one exabyte is 10 ** 18 Bytes. By convention, we measure storage and network bandwidth in base 10, and not base 2. However, the RAM of these servers is only 32 GB
**Note: the servers described above are not the only types of servers  in a data center. organizations also require servers for services like configuration, monitoring, load balancing, analytics, accounting , caching, and so on**

the numbers open-sourced by Facebook are outdated as of now. in the table below, we depict the capabilities of a server that can be used in the data centers of today
![Screenshot 2024-02-28 at 13.00.07.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Lxdd7m%2FScreenshot%202024-02-28%20at%2013.00.07.png)

**Note: hardware threads were originally called simultaneous multithreading. Later, intel rebranded it as hyper threading**
the numbers above are inspired by the Amazon bare-metal server, but there can be more or less powerful machines supporting much higher RAM (up to 8 TB) disk storage(up to 24 disks with up to 20 TB each, circa 2021), and cache memory(up to 120 MB)
## Standard numbers to remember
A lot of effort that goes into the planning and implementation of a service. but wothout any basic knowledge of the kind of workloads machines can handle, this planning is not possible. Latencies play an important role in deciding the amount of workload a machine can handle. the table below depicts some of the important numbers system designers should know in order to perform resource estimation.
![Screenshot 2024-02-28 at 13.05.06.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_khc40C%2FScreenshot%202024-02-28%20at%2013.05.06.png)

apart from the latencies listed above, there are also throughput numbers measured as queries per second that a typical single server data store can handle.
![Screenshot 2024-02-28 at 13.06.59.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_iK2yuD%2FScreenshot%202024-02-28%20at%2013.06.59.png)
the numbers above are approximations and vary greatly depending on a number of reasons like the type of query, the specification of the machine, the design of the database, the indexing and so on.

## Requests estimation
this section discusses the number of requests a typical server can handle in a second. within a server, there are limited resources and depending on the type of client requests, different resources can become a bottleneck let us understand the two types of requests
  * **CPU-bound requests:** these are the type of requests where the limiting factor is the CPU
  * **memory-bound requests: ** these are the types of requests that are limited by the amount of memory a machine has
let us approximate the RPS for each type of request. but before that, we need to assume the following
  * our server has the specifications of the typical server that we defined in the table above
  * operating systems and other auxiliary processes have consumed a total of 16 gb of ram
  * each worker consumes 300 MBs of RAM storage to complete a request
  * for simplicity, we assume that the CPU obtains data from the RAM. therefore, a caching system ensures that all the required content is available for serving, wthout there being a need to access the storage layer.
  * each CPU-bound request takes 200 miliseconds, whereas a memory-bound request takes 50 miliseconds to complete
lets do the computation

**CPU bound**: A simple formula used to calculate the RPS for CPU bound request is
  
      RPS_cpu = NUM_cpu * 1/TASK_time
where:
  **RPS_cpu**: CPU bound RPS
  **NUM_cpu** : number of CPU threads, which are als called hardware threads.
  **TASK_time**: the time each task takes to complete


      Then, RPS_cpu = 72 * 1/200ms = 360 RPS.
the rationale for that above calculation is that we can visualize one second as a box and we calculate how many mini-boxes(tasks) can fit inside the big box- that is, the number of tasks that can be completed in one second by a number of CPUs. so a higher number of CPUs / threads will result ina higher RPS

**Memory-bound requests**: for memory bound requests, we use the following formula


      RPS_memory = RAM_size / WORKER_memory * 1 / TASK_time
where
  **RPS_memory**: memory bound RPS
  **RAM_size**: total RAM size
  **WORKER_memory**: a worker in memory that manages a request.

      then RPS_memory = 240 GB / 300 MB * 1 / 50 ms = 16, 000 RPS

Continuing our box analogy, here we first calculate the number of boxes there are (how many memory bound processes a server can host) and then how many mini-boxes(tasks) we can fit in each of the bigger boxes.
A service receives both CPU-bound and memory-bound requests. considering the case that half the requests are cpu-bound and the other half memory-bound, we can handle a total of
  
      360 / 2 + 16,000 / 2 =~ 8, 000 RPS

the calculations above are only an approximation for developing an understanding of the basic factors involved in estimating RPS. in reality, a lot of other factors come into play. for instance, latency is required to do a disk seek in case the data is not readily available in RAM or if a requestis made to the database server, which also include the database and network latency. Additionally, the type of query also matters. of course, faults bugs in code, node failures, power outages, network disruptions and more are inevitable factors.

on a typical day, various types of requests arrive and a powerful server that only serves static content from the RAM might handle as many as 500k RPS . on the other day of the spectrum, computational-intensive tasks like image procesing may only allow a maximum of 50 RPS.
**Note: in reality, capacity estimation is a hard problem, and organizations learn how to improve it over the years. a monitoring system keeps an eye on all parts of our infrastructure to give us early warnings about overloading servers. **

## Examples of Resource estimation
### Number of servers required

let us make the following assumptions about a twitter like service

  * there are 500 million daily active users
  * a single user makes 20 requests per day on average
  * recall that a single server can handle 8000 RPS
![Screenshot 2024-02-28 at 13.34.10.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Ch9RuJ%2FScreenshot%202024-02-28%20at%2013.34.10.png)

# Building Blocks

system design is like using Lego pieces to make bigger fascinating artifacts

## The bottom-um approach for modern system design.
system design problems normally have some similarities, though specific details are often unique. we have extracted these similarities across design problems as the basic building blocks we will be covering. One example of a building block is a load-balancing component, which we will probably use i every design problem in one way or the other. 

the purpose of separating the buildng blocks is to thoroughly discuss their design just once. this means that later we can use them anywhere without having to go over them in detail again. we can think about building blocks as bricks to construct more effective capable systems. 

many of the building blocks we discuss are also available for actual  use in the public clouds, such as Aws, Azure, and Google cloud platform. we can use such constructs to build a system to further cement our understanding 

**Domain Name System**: this focuses on how to design hierarchical and distributed naming system for computers connected to the internet via different internet protocols
**Load balancers**: here, we will understand the design of a load balancer, which is used to fairly distribute incoming clients requests among a pool of available servers. it also reduces load and can bypass failed servers.
**Databases**: this enables us to store, retrieve, modify  and delete data in connection with different data processing procedures. here we will discuss database types, replication, partitioning, and analysis of distributed databases. 
**key-value store**: this is a non-relational database that stores data in the form of a key-value pair. here we will explain the design for a key-value store along with important concepts such as achieving scalability, durability, and configurability.
**content-delivery-network**: here, we will design a CDN that is used ot keep viral contents such as videos, images, audio, and webpages. it efficiently delivers content to end users while reducing latency and burden on the data centers.
**sequencer**: here we will focus on the design of a unique IDs generator with a major focus on maintaining causality. it also explains three different methods for generating unique IDs
**service-monitoring**: monitoring systems are critical in distributed systems because they help analyze the system and alert the stakeholders if a problem occurs. Monitoring is often useful to get early warning signs so that system administrators can act ahead of an impending problem becoming a huge issue. here, we will build two monitoring systems, one for the server side and the other for the client-side errors
**distributed caching**: in this building block, we will design a distributed caching system where multiple cache servers coordinate to store frequently accessed data.
**distributed messaging queue**: in this building block, we will focus on the design of a queue consisting of multiple servers, which is used between interacting entities called producers and consumers. it helps decouple producers and consumers, results in independent scalability and enhances reliability.
**publish-subscribe system**: here we will focus on the design of an asynchronous service to service communication method called a pub-sub system. it is popular in serverless, microservices architectures and data processing systems.
**rate-limier**: here we will design a system that throttles incoming requests for a service based on the predefined limit. it is generally used as a defensive layer for services to avoid their excessive usage-whether intended or unintended.
**Blob store**: this building block focuses on a storage solution for unstructured data - for example multimedia files and binary executables
**distributed search**: a search system takes a query from a user and returns relevant content in a few seconds or less. this building block focuses on the three integral components: crawl, index, and search
**distributed logging**: logging is an I/O intensive operation that is time-consuming and slow. here we will design a system that allows services in a distributed system to log their events efficiently. The system will be made scalable and reliable.
**distributed task scheduling**: we will design a distributed task scheduler system that mediates between tasks and resources. it intelligently allocates resources to tasks to meet task level and system-level goals. it is often used offload background processing to be completed asynchronously
**sharded counters**: this building block demonstarates an efficient distributed counting system to deal with millions of concurrent read/write requests, such as likes on a celebrity's tweet
these building blocks have been ordered topologically so the building blocks that depende on others come later.

## Conclusion
for elaboration, we will use a "requirements" section whenever we design a building block (and a design problem). the requirements section will highlight the deliverables we expect from the developed design . requirements will have two sub categories.
**functional requirements** These represent the featres a user of the designed system will be able to use. foe example, the system will allow a user to search for content using the search bar
**Non-functional requirements**: this is a criteria based on which the user of a system will consider the system usable. NFR may conclude requirements like high availability, low latency, scalability, and so on. 

# Introduction to Domain Name System(DNS)
here we will learn how domain names, get translated to IP addresses through DNS

## the origin of DNS
- let us consider the example of a mobile phone where a unique number is associated with each user. to make calls to friends, we can initially try to memorize some of the phone numbers. However, as the number of contacts grows,  we will have to use a phone book to keep track of all our contacts. This way, whenever we need to make a call, we will refer to the phone book and dial the number we need. 
- Similarly, computers are uniquely identified by IP addresses - for example, ```104.18.2.119``` is an IP address. we use ip addresses to visit a website hosted on a machine. since humans cannot easily remember IP addresses to visit domain names(an example being google.com) we need a ohone book- like repository that can maintain all mappings of domain names to IP addresses. here, we will see how DNS serves as the internets phonebook
![Screenshot 2024-02-29 at 11.41.24.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_TQUYEL%2FScreenshot%202024-02-29%20at%2011.41.24.png)

## what is DNS
the **domain name system** is the internet's naming service that maps human-friendly domain names to machine-readble ip addresses. the service of DNS is transparent to users. when a user enters a domain name in the browser, the browser has to translate the domain name to ip address by asking the DNS infrastructure. once the desire ip address is obtained, the user's request is forwarded to the destination web server.
![Screenshot 2024-02-29 at 11.45.31.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_4Vg0qA%2FScreenshot%202024-02-29%20at%2011.45.31.png)
the entire operation is performed very quickly. therefore, the end user experiences minimum delay. we will also see how browsers save some of the frequently used mappings for later use.

## important details
**Name servers:** it is important to understand that the DNS is not a single server. it is a complete infrastructure with numerous servers. DNS servers that respond to user's queries are called name servers
**resource records:** the DNS database stores domain name to IP address mappings in the form of resource records. the RR is the smallest unit of information that users request from the name servers. there are different types of RRs. the table below describes common ones. the three important pieces of information are type, name, and value. the name and value change depending upon the type of the RR
* **caching**: DNS uses caching at different layers to reduce request katency for the user. caching plays an important role in reducing the burden on DNS infrastructure because it has to cater to the queiries of the entire internet. 
* **hierarchy**: DNS name servers are in a hierarchical form. the hierarchical structure allows DNS to be highly scalable because of its increasing size and query load. we will look at how a tree-like structure is used to manage the entire DNS database

## how DNS works
let us now try to understand how the domain name system works
we seek to answer the following questions
* how is the DNS hierarchy formed using various types of DNS name servers?
* how is caching performed at different levels of the internet to reduce the querying burden over the DNS infrastructure?
* how does the distributed nature of the DNS infrastructure help its robustness?
## DNS hierarchy
the DNS is not a single server that accepts requests and responds to user queries. it is a complete infrastructure with name servers at different hierarchies
there are mainly four types of servers in the DNS hierarchy:
* **DNS resolver:** Resolvers initiate the querying sequence and forward requests to the other DNS name servers. Typically, DNS resolvers lie within the premise of the user's network. However, DNS resolvers can also cater to user's DNS querires through caching techniques, as we will se shortly. These servers can also be called local or default servers
* **root-level name servers**: these servers receive requests from local servers. Root name servers maintain name servers based on top-level domain names such as ```.com```, ```.edu```, ```.us``` and so on. for instance, when a user requests the ip address of educative.io, root-level name servers will return a list of top-level domain(TLD) servers that hold the ip addresses of the .io domain
* **Top level domain name server**: these servers hold the ip addresses of authoritative name servers. the querying party will get a list of Ip addresses that belong to the authoratative name servers of the organization. 
* **authoritative name servers:** these are the organization's DNS name servers that provide the IP addresses of the web or application servers
![Screenshot 2024-02-29 at 12.42.48.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_LAxqX2%2FScreenshot%202024-02-29%20at%2012.42.48.png)

DNS names are processed from right to left. 

## Iterative versus recursive query resolution
there are two ways to perform a DNS query
* **iterative**: the local server requests the root  TLD, and the authoritative servers for the ip address
* **recursive:** the end user requests the local server. the local server further requests the root DNS name servers. the root name servers forward the requests to the other name servers
* in the following illustration(on the left), DNS query resolution is iterative from the perspective of the local/isp server
![Screenshot 2024-02-29 at 12.48.42.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_yuEcXG%2FScreenshot%202024-02-29%20at%2012.48.42.png)

**Note: typically, an iterative query is performed to reduce query load oon DNS infrastructure.**

Fun fact **These days we will find many third-party public DNS resolvers offered by google, cloudflare, OpenDNS and many more. the interesting fact is that public DNS servers may provide quicker responses thatn the local ISP DNS facilities**


## Caching
**caching** refers to the temporary storage of frequently requested resource records. a record is a data unit within he DNS database that shows a name-to-value binding. caching reduces response time to the user and decreases network traffic. when we use caching at different hirearchies, it can reduce a lot of querying burden on the DNS infrastructure. caching can be implemented in the browser, operating systems, local name server within the user's network or the ISP's DNS resolvers. 
below is a demonstration of the power of caching in the DNS
![Screenshot 2024-02-29 at 12.57.08.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_v10Xgc%2FScreenshot%202024-02-29%20at%2012.57.08.png)


**Note: Even if there is no cache available to resolve a user's query and it is imperative to visit the DNS infrastructure, caching can still be beneficial. the local server or ISP DNS resolver can cache the ip adderesses of the tLD servers or authoratative servers and avoid requesting the root-level server. **


## DNS is a distributed system
although the DNS hierarchy facilitates the distributed internet that we know today, it is distributed system itself. the distributed anature of DNS has the following advantages
* it avoids becoming a single point of failure
* it achieves low query latency so users can get responses from nearby servers
* it gets a higher degree of flexibility during maintenance and updates or upgrades. for example, if one DNS server is down or overburdened, another DNS server can respond to user queries.
there are 13 logical root name servers named letter A through M with many instances spread throughout the globe. these servers are managed by 12 different organizations.

## Hghly scalable
due to its hierarchical nature, DNS is a highly scalable system. roughly 1,000 replicated instances of 13 root-level servers are spread throughout the world startegically to handle user queries. the working loabor is divided among TLD and root servers to handle a query and, finally the authoritattive servers that are managed by the organisations themselves to make the entire system work. as shown in the DNS hierarchy tree above, different services handle different portions of the tree enabling scalability and manageability of the system.
## Reliable
the DNS is reliable because:
* **caching**: The caching is done in the browser, the operating system, and the local name server, and the isp DNS resolvers also maintain a rich cache of frequently visited services. even if some DNS servers are temporarily dow, cached records can be served to make DNS a reliable system.
* **server replication**: DNS has replicated copies of each logical server spread systematically across the globe to entertain user requests at low latency. the redundant servers improve the reliability of the overall system.
* **protocol**: although many clients rely on the unreliable user datagram protocol(UDP) to request and receive DNS responses, it is important to acknowledge that udp also offers distinct advantages. udp is much faster and, therefore, improves DNS peformance. furthermore, internet service's reliability has improved since its inception, so udp is usually fovored over TCP . a DNS resolver can resend the udp request if it did not get a reply to a prevois one. this request-response needs just one round trip which provides a shorter delay as compared to TCP, which needs a three-way handshake before data exchange.
should DNS continue using UDP in case of a network congestion? **typically, DNS used UDP. however, DNS can use TCP when its message size exceeds the original packet size of 512 bytes. this is because large-size packets are more prone to be damaged in congested networks, DNS always uses tcp for zone transfers.**

## Consistent
DNS uses various protocols to update and transfer information among replicated servers in a hierarchy. DNS compromises on strong consistency to achieve high performance because data is read frequently from DNS databases as compared to writing. however, DNS provides eventual consistency and updates records on replicated servers lazily. typically, it can take from a few seconds up to three days to update records on the DNS servers across the internet. the time it takes to propagate information among different DNS clusters depends on the DNS infrastructure, the size of the update, and which part of the DNS tree is being updated.
consistency can suffer because of caching too. since authoritative servers are located within the organization, it may be possible that certain resource records at the default/local and isp servers may be outdated. to mitigate this issue, each cached record comes with an expiration time called **time-to-live**
**to maintain high availability, the TTL value should be small. this is because if any server or cluster fails, the organization can update the resource records right aay. users will experience non-availability only for the time the TTL is not expired. however, if the ttl is large, the organization will update its resource records, whereas users will keep pinging the outdated server that would have crashed long ago. companies that long for high availability maintain a TTL value as low as 120 seconds. therefore, even in case of a failure, the maximum downtime is a few minutes. **
 let us run the following commands
```
nslookup www.google.com
dig www.google.com
```


### nslookup
the ```non-authoratative asnwer```, as the name suggests, is the answer provided by a server that is not the authoritative serevr of Google. it is not in the list of authoratitive serevrs that google maintains. so, wehre does the asnwer come from? the asnwer is provided by second, third, and fourth-hand name servers configured to reply to our DNS query - for example, our university or office DNS resover, our isp nameserver, our isp's isp nameserver, and so on. in short, it can be considered as a cached version of google's authoritative nameserver response. if we try multiple domain names, we will realize that we recieved a cached response most of the time. 
if we run the same command multiple times, we will recieve the same ip addresses list but in a different order each time. the reason for that is DNS is indirectly performing load balancing. it is an important term that we will gain familiarity with in the coming lessons.

## the dig output
the ```query time: 4sec``` represents the time it takes to get a response from the DNS server. for various reasons, the numbers may be differnet in our case.
the ```300``` value in the ```answer section``` represents the number of seconds the cache is maintained in the DNS resolver. this means that Google's ADNS keeps a ttl value of five minutes(33 sec / 60)
**Note: we invite you to test different services for their TTL and query times to strengthen your understanding. you may use the above terminal for this purpose**

**Question:** if we need DNS to tell us which IP to reach a website or service, how will we know the DNS resolver's ip address? (it seems like a chicken-and-egg problem)
**Answer:** 

# Introduction to load balancers
here we will learn the basics of load balancers and the services they offer

## What is load balancing
millions of requests could arrive per second in a typical data center. to server these requests, thousands of servers work together to share the load of incoming requests.
**Note: here, it is important that we consider the incoming requests will be divided among all the available servers**
a **load balancer B** is the answer to the question. The job of the load balancer is to fairly divde all client's reqeusts among the pool of available servers. load balancers perform this job to avoid overloading or crashing servers

the load balancing layer is the first point of contact within a data center after the firewall. a load balancer may not be required if a service entertains few hundred or thousand requests per second. however, for increasing client requests, load balancers provide the following capabilities.
* **scalability**: By adding servers, the capacity of the application can be increased seamlessly. load balancers make such upscaling or downscaling transparent to the edn user.
* **availability**: even if some servers go down or suffer a fault, the system still remains available. one of the jobs of load balancers is to hide faults and failures of servers
* **performance:** load balancers can forward requests to servers with a lesser load so the user can get a quicker response time. this not only improves performance but also improves resource utilization.
here is an abstract depiction of how load balancers work
![Screenshot 2024-02-29 at 15.01.57.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_YurFlq%2FScreenshot%202024-02-29%20at%2015.01.57.png)
## placing load balancers
Generally, LBs sit between clients and servers. Requests go through to servers and back to clients via load balancing layer. However, this is not the only point where load balancers are used.
let us consider the three well-nown groups of servers. that is the web, the application, and the database servers. to divide the traffic load among the available servers, load balancers can be used between the server instances of these three in the followinf ways
  * place LBs between end users of the application and web servers/application gateway
  * place LBs between the web servers and application servers that run the business/application logic
  * place LBs between the application servers and database servers
![Screenshot 2024-02-29 at 15.06.43.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_2VetZh%2FScreenshot%202024-02-29%20at%2015.06.43.png)
in reality, load balancers can be potentially used between any two services with multiple instances within the design of a system.

## services offered by load balancers
LBs not only enable services to be scalable, available, and highly performant, they offer some key services like the following
  * **health checking:** LBs use the heartbeat protocol to monitor the health and, therefore, reliablity of end-servers. another advantage of health checking is the improved user experience
  * **TLS termination:** LBs reduce the burden on end-servers by handling TLS termination with the client.
  * **predictive analysis:** LBs can predict traffic patterns through analytics performed over traffic passing through them or using statistics of traffic obtained over time.
  * **reduced human intervention:** because of a LB automation, reduced system administration efforts are required in handling failures
  * **service discovery:** an advantage of LBs is that the client's requests are forwarded to appropriate hosting servers by inquiring about the servce registry. 
  * **security:** LBs may also improve security by mitigating attacks like denial-of-service at different layers of the OSI model.
as a whole, load balancers provide; flexibility, reliability, redundancy, and efficiency to the overall design of the system. 
are LBs a single point of failure? 
  * **LBs are usually deployed in pairs asa means of disaster recovery. if one load balancer fails, and there is nithing to failover to, the overall service will go down. Generally, to maintain high availability, enterprises use clusters of load balancers that use heratbeat communciation to check the health of load balancers at all times. on failure of primary LB, the back up can take over. But if the entire cluster fails, manual rerouting can also be performed in case of emergencies**
## Global and local Load balancing
here we will understanding how global and local load balancing works

### Introduction
from the previous lesson, it may seem like load balancing is performed only within the data center. However, load balancing is required at a global and a loacl scale. let us understand the function of each of the two.
  * **Global server load balancing (GSLB)**: GSLB involves the distribution of traffic load across multiple geographical locations
  * **local load balancing:** this refers to load balancing achieved within a data center. this type of load balancing focuses on improving efficency and better resource utilization of the hosting servers in a data center.

## Global server load balancing
GSLB ensures that globally arriving traffic load is inteligetly forwarded to a data center. for example, power or network failure in a data center requires that all the traffic be routed to another data center. GSLB takes forwarding decisions based on the user's geographic locations, the number of hosting servers in different locations, the health of data centers and so on.
in the next lesson, we will also learn how GSLB offers automatic zonal failover. GSLB service can be installed on-premise or obtained through load balancing as a service.
the illustration below shows that the GSLB can forward requests to three different data centers. Each local load balancing layer within a data center will maintain a control plane connection with the GSLB prociding information about the health of the LBs and the server farm. GSLB uses this information to drive traffic decisions and forward traffic load based on each regions configuration and monitoring information. 

![Screenshot 2024-02-29 at 16.04.30.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_cy9cYS%2FScreenshot%202024-02-29%20at%2016.04.30.png)

## Load balancing in DNS
we understand that DNS can respond with multiple ip addresses for a DNS query. in the lesson on DNS, we discussed that it is possible to do load balancing through DNS while looking at the output of ```nslookup```. DNS uses a simple technique of reordering the list of ip addresses in response to each DNS query. therefore, different users get a reordered ip address list. it results in users visiting a different server to entertain their requests. in this way, DNS uses round-robin to perform load balancing as shown below. 

![Screenshot 2024-02-29 at 16.09.46.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_Bgb6YV%2FScreenshot%202024-02-29%20at%2016.09.46.png)
As shown above, round-robin in DNS forwards clients to data centers in a strict circular order. however, round -robin has the following limitations
  * different isps have different number of users. an isp serving many customers will provide the same cached ip to its clients, resulting in uneven load distribution on end servers.
  * because the round-robin load-balancing algorithm does not consider any end-server crashes, it keeps on distributing the ip address of the crashed servers untill the TTL of the cached entries expires. availability of the service, in that case, can take a hit due to DNS-level load balancing
despite its limitations, round-robin is still widely used by many DNS service providers. furthermore, DNS uses short TTL for cached entries to do effective load balancing among different data centers.
  * **Note: DNS is not the only form of GSLB. application delivery controllers(ADCs) and cloud based load balancing are better ways to do GSLB**

## The need for local load balancers
DNS plays a vital role in balancing the load, but it suffers from the following limitations
  * the small size of the DNS packets is not enough to include all possible ip addresses of the servers
  * there is limited control over the client's behaviour. clients may select arbitrarily from the received set of ip addressses. some of the received ip addresses may belong to busy data centers.
  * clients cannot determine the closes address to establish a connection with. Although DNS geolocation and anycasting-like solutions can be implemented, they are not trivial solutions.
  * in case of failures, recovery can be slow through DNS because of the caching mechanism, especially when TTL values are longer

to solve some of the above problems, we need another layer of load balancing in the form of local LB. in the next lesson we will discuss differnet details about local load balancers

## what is local load balancing
local load balancers reside within a data center. they behave like a reverse proxy and make their best effort to divide incoming requests among the pool of available servers. incoming clients' requests seamlessly connect to the LB that uses virtual IP address.

can DNS be considered global server load balancer? **yes, there are actually two ways of doing global traffic management:**
  * **GTM through ADCs**: some ADCs implement GSLB. in that case ADCs have a real-time view of the hosting servers and forward requests based on the health and capacity of the data center.
  * **GTM through DNS**: DNS does GSLB by analyzing the ip location of the client. for each user requesting ip for a domain name, dns-based gslb forwards the ip address of the data center geographically closer to the requesting ip location.

## Advanced Details of local load balancers
here we will understand load balancers and their usage within a system. we will focus on some of the well-known algorithms used in the local load balancers. we will also understand how load balancers are connected to for a heirarchical, sharing work across different tiers of LBs

## Algorithms of load balancers
load balancers distribute client requests according to an algorithm. some well-known algorithms are given below
* ****



































