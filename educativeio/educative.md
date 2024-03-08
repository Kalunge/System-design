# Introduction to Modern System Design
## What is system Design
**System Design** is the process of defining components and their integration, APIs, and data models to build large scale systems that meet a specified set o
f functional and non functional requirements.
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
* **Round-robin scheduling**: in this algorithm, each request is forwarded to a server in the pool in a repeating sequential manner
* **weighted round-robin**: if some servers have a higher capability of serving client's requests, then it is preferred to use a weighted round-robin algorithm. here, each node is assigned a weight. LBs forward clients' requests according to the weight of the node. the higher the weight, the higher the number of assignments. 
* **least connections**: in certain cases, even if all the servers have the same capacity to serve clients, uneven load oncertain servers is still a possibility. for example, some clients may have a request that requires longer to serve. or some clients may have subsequent requests on the same connection. in that case, we can use algorithms like least connections where newer arriving requests are assigned to servers with fewer existing connections. LBs keep a state of the number and mapping of existing connections in such a scenario. we will discuss more about state maintenance later .
* **least response tme: **in performance-sensitive services, algorithms such as least response time are required. this algorithm ensures that the server with the least response time is requested to serve the clients
* **IP hash**: some applications provide a different level of service to users based on their ip addresses. in tha case, hashing the ip address is performed to assign user's requests to servers. 
* **URL hash: **it may be possible that some services within the application are provided by specific servers only. in that case, a client requesting service form a URRL is assigned to a certain cluster or set of servers. the url hashing algorithm is used in those scenarios.
there are other algorithms also, like randomized or weighted least connections algorithms
## Static vs dynamic algorithms
algorithms can be static or dynamic depending on the machine's state. let us look at each of the categories individually.
**static algorithms:** dont consider the changing state of the servers. therefore, task assignment is carried out based onexisting knowledge about the server's configuration. Naturally, these algorithms are not complex, and they get implemented in a single route or commodity machine where all the requests arrive.
**dynamic algorithms** are algorithms that consider the current or rece=nt state of the servers. dynamic algorithms maintain state by communicating with the server, which adds a mouunication overhead. state maintainance makes the design of the algorithm much more complicated.

Dynamic algorithms require different load balancing servers to communicate with each other to exchange information. therefore, dynamic algorithms can be modular because no single entity wii do the decision making. although this adds complexity to dynamic algorithms, it results in improved forwarding decisions. finally, dynamic algorithms monitor the healt of the servers and forward requests to active servers only.
**Note: in practice, dynamic algorithms provide far better results because they maintain a state of serving hosts and are, therefore, worth the effort and complexity.**

## Stateful vs stateless LBs
while static and dynamic algorithms are required to consider the health of the hosting servers, a state is maintained to hold session information of different clients with hosting servers.
if the session ifnormation is not kept at a lower layer(distributed cache or database), load balancers are used to keep the session information. below we describe two ways of handling session maintenance through LBs
* stateful
* stateless

## stateful load balancing
as the name indicates, **stateful load balancing** involves maintaining a state of the sessions established between clients and hosting servers. the stateful LB incorporates state information in its algorithm to perform load balancing.
essentially, the stateful LBs retain a data structure that maps incoming clients to hosting servers . stateful LBs increase complexity and limit scalability because session information of all the clients in maintained across all the load balancers. that is, load balancers share their state information with each other to make forwarding decisions
![Screenshot 2024-02-29 at 18.02.20.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_qOBSRy%2FScreenshot%202024-02-29%20at%2018.02.20.png)


## stateless load balancing
**stateless load balancing** maintains no state and is therefore, faster and lightweight. stateless load balancers use consistent hasshing to make forwarding decisions. However, if infrasturcture changes(for example, a new application server joining)
 stateless LBs may not be as resilient as stateful  liad balancers because consistent hashing alone is not enough to route a request to the correct application server. therefore, a local state may still be required with consistent hashing
![Screenshot 2024-02-29 at 18.05.55.png](..%2F..%2F..%2FScreenshot%202024-02-29%20at%2018.05.55.png)
therefore, a state maintained across different load balancers is considered a stateful load balancing. wehreas a state maintained within a load balancer for internal use is assumed as stateless load. 

## types of load balancers
depending on the requirements, load balancing can be performed at the network/transport and application layer of the open systems interconnection layers.
**layer 4 load balancers**: layer 4 refers to the load balancing performed on the basis of transport protocols like TCP and UDP. these types of LBs maintain connection/session with the clients and ensures that he same(TCP/UDP) communication ends up being forwarded to the same back-end server. even though TLS terminatio is performed at layer 7 LBs, some layer 4 LBs also transport it.
**layer 7 LBs** layer 7 LBs are based on the data of the application layer protocols. it is possible to make application-aware forwarding decisions based on HTTP headers, urls, cookies, and other application specific data-for example, user id. apart from performing tls termination, these LBs can take responsibilities like rate limiting users, http routing, and header rewriting.

**Note: layer 7 LBs are smart in  terms of inspection. however, layer 4 LBs are faster in terms of processing**

## Load balancer deployment
we discussed the trade-offs of load balancing performed at different OSI layers. in practice, however, a single layer LB is not enough for a large data center. in fact multiple layers of load balancers coordinate to take informed forwarding decidions. a traditional data center may have a three-tier LB as shown below
![Screenshot 2024-03-01 at 09.12.50.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_YSOhqj%2FScreenshot%202024-03-01%20at%2009.12.50.png)

## Implementation of load balancers
different kinds of load balancers can be implemented depending on the number of incoming requests, organization and application-specific requirements

## Hardware load balancers
load balancers were introduced in the 1990s as hardware devices. hardware load balancers work as stand-alone devices and are quite expemsive. nonetheless , they have their perfomrnce benefits and are able to handle a lot of concurrent users. configuration of hardware-based solutions is problematic becuase it requires additional human resources. therefore, they are not the go-to solutions even for large enterprises that can afford them. availability can be an issue with hardware load balancers because additional hardware will be required to failover to in case of failures. finally, hardware load balancers can have highrt maintainance / operational costs and compatibility issues making them less flexible. not to mention that hardware load balancers have vender locks as well

## software load balancers
software load balancers are becoming increasingly popular because of their flexibility, programmability and cost-effectiveness. that is all possible because they are implemented on commodity hardware. software load balancers scale well as requirements grow. availablity is not an issue because small additional costs are required to implement shadow load balancers on commodity hardware. additionally, software load balancers can provide predictive analysis that can help prepare for future traffic patterns.

## cloud load balancers
with the advent of the field of cloud computing , load balancers as a service has been introduced. this is where cloud owners provide load balancing services. users pay according to their usage or the service-level agreement with the cloud provider. cloud based load balancers may not necessarily replace a local on-premise load balancing facility, but they can perform global traffic management between different zones. primary advantages of such load balancers include ease of use , management metered cost, flexibility in terms of usage, auditing and monitoring services to improve business decisions. an example of how cloud based load balancers can provide GSLB is shown below
![Screenshot 2024-03-01 at 09.36.50.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_ytbc9P%2FScreenshot%202024-03-01%20at%2009.36.50.png)

# Introduction to databases.
here, we will understand what a database is and its use case in system design

## problem statement
let us start with a simple question. can we make a software application without using databases? let us suppose we have an application like whatsapp. people use our application to communicate with their friends. now, where and how we can store information permantently and retrieve it?
we can use a simple file to store all the records on separate lines and retrieve them from the same file. but using a file for storage has some limitations

## limitations of file storage
* we cannot offer concurrent management to separate users accessing the storage files from different locations
* we cannot grant different access rights to different users.
* how will the system scale and be available when adding thousands of entries?
* how will we search content for different users in a short time?
![Screenshot 2024-03-01 at 11.04.30.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_VqIcsH%2FScreenshot%202024-03-01%20at%2011.04.30.png)
## solution
these limitations can be addressed by a database.
a **database** is an organized collection of dta that can be managed and accessed easily. Databases are created to make it easier to store , retrieve, modify, and delete data in connection with different data-processing procedures.
some of the applications where we use database management are the banking systems, online shopping stores, and so on. different organizations have different sizes of databases according to their needs.

**Note: According to a source, the world data center for climate is the largest database in the world. it contains around 220 TB of web data and 6 PB of additional data**
there are two basic types of databases
* SQL(relational databases)
* NoSQL(non-relational databases)

they differ in terms of their intended use case, the type of information they hold, and the storage method they employ.
![Screenshot 2024-03-01 at 11.14.28.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_BQw1gz%2FScreenshot%202024-03-01%20at%2011.14.28.png)
Relational databases, like phone books that record contact numbers and addresses, are organized and have predetermined schemas. non-relational databases, like file directories that store anything from a person's constant information to shopping preferences are unstructured, scattered, and feature a dynamic schema. we will discuss their differences and their types in detail

## Advantages
a proper database is essential for every business or organization. this is because the database stores all essential information about the organization, such as personnel records, transactions, salary information, and so on. folowing are some of the reasons why the database is important
* managing large data
* retrieving accurate data
* easy updation
* security
* data integrity
* availability
* scalability

we will discuss
* types of databases
* data replication
* data partitioning
* cost-benefit analysis

## Types of Databases

### Relational databases
**Relational databases** adhere to particular schemas before storing the data. the data stored in Relational databases has prior structure. mostly, this model organizes data into one or more relations(tables) with aunique key for each tuple(instance). each entity of the data consists of instances and attributes, where instances are stored in rows, and the attributes of each instance are stored in columns. since each tuple has a unique key, a tuple in one table can be linked in other tables by storing the primary keys in other tables, generally known as foreign keys.

a structure query language is used for manipulating the database. this includes insertion, deletion, and retrieval of data.

relational databases are simple, robust, flexible, performant, scalable and compatible in managing general data.

Relational databases provide the atomicity, consistency, isolation, and durability(ACID) properties to maintain the integrity of the database. acid is a powerful abstraction that simplifies complex interactions wit the data and hides many anomalies(like drty reads, dirty writes, read skew, lost updates, write skew, and phantom reads) behind a simple transaction abort.

but ACID is like a big hammer by design that it is generic enough for all the problems. if some specific application only needs to deal with a few anomalies, there is a window of opportunity to use a custom solution for higher performance, though there is added complexity.

ACID In detail
**Atomicity**: a transaction is considered an atomic unit. therefore, either all the statements within a transaction will successfully execute, or none of them will execute. if a statement fails within a transaction, it should be aborted and rolled back
**Consistency**: at any given time, the database should be in a consistent state, it should remain in a consistent state after every transaction. for example, if multiple users want to view a record from the database, it should return a similar result each time.
**Isolation: ** in the case of multiple transactions running concurrently, they should not be affected by each other. the final state of the database should be the same as the transactions were executed sequentially.
**durability:** the system should guarantee that completed transactions will survive permanently in the database even in system failure events

examples: 
  * MYSQL
  * Oracle Database
  * Microsoft sql server
  * ibm db2
  * Postregs
  * SQlite

## Why relational databases
relational databases are the default choices for structured data storage. there are a number of advantages to these databaseslike its abstarction of ACID transactions and related programming semantics.this makes it very convinient foe the end-programmer to use relational databases. some important feature include

* **Flexibility**: data definition language makes it easier and possible to modify schema(tables, columns, database etc) while other queries are happening and the db server is running
* **reduced redundancy**: use of relationships helps eliminate data redundancy.
* **concurrency**: transactions being atomic helps in cases where data is read and written at the same time by many users
* **Integration**: the process of aggregation from multiple sources is a common practice in enterprise applications. a common way to perform this aggregation is to integrate a shared database where multiple applications store their data.. this way all the applications can easily access each oher's data while the concurrency control measures handle the access of multiple applciations. 
* **backup and disaster recovery**: Relational databases guarantee the state of data is consistent at any time. the export and imort operations make backup and restoration easier. most cloud-based relational databases perform contnous mirroring to avoid loss of data and make the restoration process easier and quicker

## Drawback
### Impedance mismatch
**Impedance mismatch** is the difference between the relational model and the in-memory data structures. the relational model organizes data into a tabular structure with relations and tuples. SQL operation on this structured data yields relations aligned with relational algebra. however, it has some limitaions. in particular, the values in a table take simple values that cannot be a structure or a list. the case is differnet for in-memory, where a complex data structure can be stored. to make the complex structures compatible with the relations, we would need a translation if the data in light of relational algrebra. so the Impedance requires translation between two representations, as denoted in the following figure
![Screenshot 2024-03-01 at 11.48.46.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_fPyYF8%2FScreenshot%202024-03-01%20at%2011.48.46.png)

## non relational databases?
a NoSQL is designed for a variety of data models to access and manage data. these databases are used in applications that require a large volume of semi-structured and unstructured data, low latency, and flexible data models. this can be achieved by relaxing some of the data consistency restrictions of other databases. 

* **simple design** unlike relational databases NoSQL does not require dealing with the impedance mismatch-for example storing all the employees' data in one document instead of multiple tables that require join operations. this strategy makes it simple and easier to write less code, debug, and maintain
* **horizontal scaling**: Primarily, NoSQL is preferred due to its ability to run databases on a large cluster. this solves the problem when the number of concurrent users increases. NoSQL makes it easier to scale out since the data related to a specific employee is stored in one document instead of multiple tables over nodes. NoSQL databases often spread data across multiple nodes and balance data and queries across nodes automatically. in cse of a node failure, it can be transparently replaced without any application disruption.
* **availability**: to enhance the availability of data, node replacement can be performed without application downtime. most of the non-relational databases variants support data replication to ensure high availability and disaster recovery.
* **support for unstructured and semi-structured data**: many NoSQL databases work with data thatdoes not have schema at the time of databse confguration or data writes. for example, document databases are structureless, they allow documents to have different fields. for example, one JSON document can have fewer fields than the other.
* **cost**: licenses for many RDBMSs are pretty expensive, while many NoSQL databases are open source and freely available. similaryl, some RDBMSs rely on costly proprietary hardware and storage systems, whle NoSQL databases use clusters of cheap commodity servers.

NoSQL databases are divided into various categories based on the nature of the operations and features, including document store, columlar store, key-value store, and graph database. we will discuss each of them along with their use cases from the system design perspective.

## Types of NoSQL databases
![Screenshot 2024-03-01 at 12.02.58.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_pXFLp2%2FScreenshot%202024-03-01%20at%2012.02.58.png)

## Key-value database
**Key-value databases** use key-value methods like hash tables to store data in key-value pairs. we can see the depicted in the figure below. here the key servs as a unique or primary key and the values can be anything ranging from simple scalar values to complex objects. these databases allow easy partitioning and horizontal scaling of the data. some pupular key-value databases include Amazon DynamoDB, and Memcached DB.
  **use case** - Key-value databases are efficient for session-oriented applications. session-oriented applications, such as web applications, store user's data in the main memory or ina database during a session. this data may include user profile information, recommendations, targeted promotions, discounts, and more. a unique ID is assigned to each user's session for easy access and storage. therefore, a better choice to store such data is the key-cvalue database
the following figure shows an example of a key-value database. the productID and Type of the ite are collectively considered as the primary key. this is considered as the key for the key-value database. moreover, the schema for storing item attributes is define based on the nature of the item and the number of attributes it possesses.
![Screenshot 2024-03-01 at 12.11.02.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_4jzslX%2FScreenshot%202024-03-01%20at%2012.11.02.png)

## Document database
A **Document database** is designed to store and retrieve documents in formats like XML, JSON, BSON, and so on. these documents are composed of a heierarchical tree data structure that can include maps, collections, and scalar values. Documents in this type of database may have varying structrues and data. Mongodb and google cloud firestore are examples of Document databases
  **use case**: Document databases are suitable for unstructured catalog datam like json files or other complex structured hierarchical data. for example, in e-commerce applications a product has thousands of attributes, which is unfeasible to store in a relational database due to its impact on the reading perormance. here comes the role of a dcoument database, which can efficiently store each attribute in a single file for easy management and faster reading speed. moreover, it is also a good option for content management applications, such as blogs and video platforms. an entity required for the application is stored as a single docy=ument in such applications.
![Screenshot 2024-03-01 at 12.18.21.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_AZ3H6O%2FScreenshot%202024-03-01%20at%2012.18.21.png)

## Graph database
**## Graph databases** use the graph data structure to store data, where nodes represent entities, and edges show relationships bewtween entities. the organization of nodes based onrelationships leads to interesting patterns between the nodes. this database allows us to store the data once and then interpret it differnetly based on relationships. popular graph databases include Noe4j OrientDB, and InfiniteGraph. graph data is kept in store files for persistenc storage. each of the files contains data for a specific part of the graph, such as nodes, links, properties and so on. 
in the following figure, some data is stored using a grah data structure in nodes connected to each other via edges rerpesenting relationships between nodes. each node has some properties, like name, ide and age. the node having id:2 has the name of James and age of 29 years
![Screenshot 2024-03-01 at 12.25.01.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_q7S5JZ%2FScreenshot%202024-03-01%20at%2012.25.01.png)

  **use case**: Graph databases can be used is social applications and provide interesting facts and figures among different kinds of users and their activities. the focus of graph databases is to store data and pave the way to drive analyses and decisions based on relationships between entities. the nature of graph databases makes them suitable for various applications, such as data regulation and privacy, machine learning research, financial services-based applications and many more
## Columnar database
**Columnar databases** store data in columns instead of rows. they enable access to all entries in the database column quickly and efficiently. popular Columnar databases include cassandra, HBase, Hypertable and Amazon redshift.
  **use case**: Columnar databases are efficient for a large number of aggregation and data analytics queries. it drastically reduces the disk I/O requirements and the amount of data require to load from the disk. for example, in applications related to fincancial institutions, there is a need to sum the financial transaction over a period of time. Columnar databases make this operation quicker by just reading the column for the amount of money, ignoring other attributes of the customers. 
the following figure shows an example of a Columnar database, where data is stored in a column-oriented format. this is unlike relational databases, whch store data in a row oriented fashion
![Screenshot 2024-03-01 at 12.33.15.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_VjqnTM%2FScreenshot%202024-03-01%20at%2012.33.15.png)

## Drawbacks of NoSQL databases
* **lack of standardization**: NoSQL doesnt follow any specific standard, like how relational databases follow relational algebra. porting applications from one type of NoSQL database to another might be a challenge.
* **Consistency: **NoSQL databases provide different products based on the specific trade-offs betwee consistency and availability when failures can happen. we wont have strong data integrity , like primary and referential inegrities in a relational database. data might not be strongly consistent but slowly converging using a weak model like eventual consistency. 

## Choosing the right database
![Screenshot 2024-03-01 at 12.40.11.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_FbWEtM%2FScreenshot%202024-03-01%20at%2012.40.11.png)

# Data replication
here we will understand the models through which data is replicated across several nodes. 
 Data is an asset for an organization because it drives the whole business. data provides critical business insights into what is important and what needs to be changed. organizations also need to securely save and server their clients' data on demand. timely access to the required data under varying condiitions is required to successfully run an online business.
we need the following characteristics from our data store.
  * availability under faults
  * scalability
  * performance
it is challenging or even impossible to achieve the above characteristics on a single node.
## Replication
**Replication** refers to keeping multiple copies of the data at various nodes(preferrably geographically distributed) to achieve availability scalability and performance. in this lesson, we assume that a single node is enough to hold our entire data. we wont use this assumption while discussing the partitioning of data in multiple nodes. often, the concepts of replication and partitioning go togterher. 
however, with many benefits, like availability, replication comes with its complexities. replication is relatively simple if the replicated data does not require frequent changes. the main problem in replication arises when we have to maintain changes in the replicated data over time.
additional complexities that could arise due to replication are as follows
  * how do we keep multiple copies of data consistent with each other?
  * how do we deal with failed replica nodes?
  * should we replicate syncrounously or asynchronously
    * how do we deal with replications lag in case of asynchronous replication
  * how do we handle concurrent writes?
  * what consistency model needs to be exposed to the end programmers?
![Screenshot 2024-03-01 at 15.17.17.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_em8rkR%2FScreenshot%202024-03-01%20at%2015.17.17.png)

## synchronous vs asynchronous replication
there are two ways to disseminate changes to the replica nodes
  * synchronous replication
  * asynchronous replication
in **synchronous** replication, the primary node waits for acknowledgement from secondary nodes about updating the data. after receiving the aknowledgement from all secondary nodes, the primary node reports success to the client. whereas in **asynchronous** replication, the primary node does not wait for the acknowledgement from the secondary nodes and reports success to the client after updating itself.
the advantage of synchronous replication is that all the secondary nodes are completely up to date with the primary node,. however there is a disadvantage to this approach. if one of the secondary nodes doe not acknowledge due to failure or fault in the network, the orimary node will be unable to acknowledge the client untill it receives the successful acknowledgeent from the crashed node. this causes high latency in the response from the primary node to the client.
on the other hand, the advantage of asynchronous replication is that the primary node can continue its work even if all the secondary nodes are own. however, if the primary node fails, the writes that werent copied to the secondary nodes will be lost.
the graph below explains the tradeoffs between data consistency and availability when different components of the sysetm can fail.
![Screenshot 2024-03-01 at 15.25.05.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_t8EBcf%2FScreenshot%202024-03-01%20at%2015.25.05.png)

## Data replication models
* single leader or primary-secondary replication
* multi -leader replication
* peer-peer or leaderless replication

## single leader or primary-secondary replication

in **primary-secondary replication**, data is replicated across multiple nodes. one node is designated as the primary. it is responsible for processing any writes to data stored on the cluster. it also sedns all the writes to the secondary nodes and keeps them in sync.
primary-secondary replication is appropriate when ou workload is read-heavy. to better scale with increasing readers, we can add more followers and distribute the read load across the available followers. However, replicating data to many followers can make a primary bottleneck. additionally, primary-secondary replication is inappropraite f pur workload is write-heavy.
another advantage of primary-secondary replication is that it is read resilient. secondary nodes can still handle read requests in case of primary node failure. therefore, it is a helpful approach for read-intensive applications.
replication via this approach comes with nconsistency if we use asynchronous replication. clients reading from different replicas may see inconsistent data in the case of failure of the primary node that couldnt propagate updated data to the secondary nodes. so if the primary node fails, any missed updates not passed on to the secondary nodes can be lost.
![Screenshot 2024-03-01 at 15.51.55.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_b1Rz71%2FScreenshot%202024-03-01%20at%2015.51.55.png)
**question:** what happen when the primary node fails?
**answer:** a secondary node can be appointed as primary node, which speeds up the rocess of recovering the initial primary node. there are two approaches to select new primary node; manual or automatic. in a **manual approach**, an operator decides which node should be the primary node and notifies all secondary nodes.. in an **automatic approach**, when secondary nodes find out thet the primary node has failed, they appoint the new primary node by conducting an election known as a leader election

### primary-secondary replication methods
* statement-based replication
* write ahead log(WAL) shipping
* Logical(row based)replication

#### statement-based replication
**statement-based replication** is an approach used in MySQL databases. in this approach the primary node executes the sql statements such as insert, update, delete
and then the statements are written into a log file. in the next step, the log file is sent to the secondary nodes for execution. this type of replication was used in MySQL before v5.1.
while this type of replication seems good, it also has some disadvantages. for example, any nondeterministic functions such as NOW() might result in distinct writes on the primary and secondary nodes. 
**Note: the NOW() function returns the current date and time according to the system clock**

#### write ahead log(WAL) shipping
**write ahead log(WAL) shipping** is a data replication technique used in both postgresql and oracle. in this technique, when a transaction occurs, it is initailly recorded in a transactional log file, and the log file is written to disk. subsequently, the recorded operations are executed on the primary database before being transmitted to secondary nodes for execution. unlike SBR , WAL maintains transactional logs instead of SQL statements into a log file, ensuring consistency when dealing with nondeterministic functions. writing to disk also aids in recovery in case of crash failures.
for example, when an operation like an UPDATE is executed in postgreSQL, it is first written to the transaction log file and disk before being applied to the database. this entry in the transaction log can include details such as the transaction ID, operation type, affected table, and new values, after which the changes are replicated to the secondary nodes. however, the drawback of WAL is its tight coupling with the inner structure of the database engine, making software upgrades on the leader and followers complicated.

#### Logical(row0based) replication
**Logical(row0based) replication** is utilised in various relational databases, including postgresql and mysql. in this approach, changes made to the database are captured at the level of the individual rows and then replicated to the secondary nodes. istead of replicating the actual physical changes made to the database., this approach captures the operations in a logical format and then executes them on secondary nodes.
for example, when operations like INSERT, or UPDATE are performed, the entire affected row is captured on the primary node, containing all the column values of the specified row. this captured change is then executed on secondary nodes, where they ensure that the data remains consistent with the data on the primary node. it offers advantages in terms of flexibility and compatitbility with different types of schemas.

## multi-leader replication
as discussed above, single leader replication using asynchronous replication has a drwback. there is only one primary node, and all the writes have to go through it, which limits the performance. in case of failure of the primary node, the secondary nodes may not have the updated database.
**multi-leader replication** is an alternative to single leader replication. there are multiple primary nodes that process the writes and send them to all other primary and secondary nodes to replicate. this type of replication is used in databases along with external tools like the Tungsten Replication for MySQL
this kind of replication is quite useful in applications in which we can continue work even if we are offline-for exampl, a calendar application in which we can set our meetings even if we dont have access to the internet. once we are online, it replicates it changes from our local database (our mobile phone or laptop acts as primary node) to other nodes
![Screenshot 2024-03-01 at 16.23.44.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_fpPXDH%2FScreenshot%202024-03-01%20at%2016.23.44.png)

## conflict
multi-leader replication gives better performance and scalability than single leader replication, but it also has a significant disadvantage. since all the primary nodes concurrently deal with the requests, they may modify the same data, whch can create a conflict between them. for example, suppose the same data is edited by two clients simultaneously. in that case, their writes will be successful in their associated primary nodes, but when they reach other primary nodes asynchronously, it creates a conflict

### Handle conflicts
conflicts can result in different data at different nodes. these should be handled efficiently without losing any data. 
![Screenshot 2024-03-01 at 16.27.45.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_YiE7ne%2FScreenshot%202024-03-01%20at%2016.27.45.png)
### conflict avoidance
a simple strategy to deal with conflicts is to prevent them from happening in the first place. conflicts can be avoided if the application can verify that all writes for a given record go via the same leader. 

However, the conflict may still occur if a user moves to a different location and is now near a different data center. if that happens, we need to reroute the traffic. in such scenarios, the conflict avoidance approach fails and results in concurrent writes. 

### Last-write wins
Using their local clock, all nodes assign a timestamp to each update. when a conflict occurs, the update with the latest timestampis selected.
this approach can also create difficulty becuse the clock synchronization across nodes is challenging in distributed systems. there is clock skew that can result in data loss.

### multi-leader replication topologies
there are many topologies through which multi-leader replication is implemented, such as circular topology, star topology, and all-to-all topology. the most common is the all-to-all topology. in start and circular topology, there is again a smililar drawback that if one of the nodes fails, it can affect the whole syste. that is why all-to-all is the most used topology.

## peer-to-peer / leaderless replication
in primary-secondary replication, the primary node is a bottleneck and a single point of failure. moreover, it helps to acheieve read scalability but fails to provide write scalability. the **peer-to-peer replication** model resolves these problems by not having a single primary node. all the nodes have equal weightage and cn accept read and write requests. this replication schema can be found in the cassandra database.
![Screenshot 2024-03-01 at 16.38.12.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_eMuKIT%2FScreenshot%202024-03-01%20at%2016.38.12.png)
like primary-secondary replication, this replication can also yield inconsistency. this is because when several nodes accept write requests, it may lead to concurrent writes. a helpful approach used for solving write-write inconsistency is called quorums

### quorums
let us suppose we have three nodes. if at least two out of three nodes are guaranteed to return successful updates, it means only one node has failed. this means that if we read from two nodes, atleast one of them will have the updated version, and our system can continue working. 
if we have n nodes, that every write must be updated in at least w nodes to be considered a success, amd we must read from r nodes. we will get an updated value from reading as long as w + r > n because at least one of the nodes must have an updated write from which we can read. quorum reads and writes adhere to these r and w values. these n, w and r are configurable in Dunamo-styled databases. 
![Screenshot 2024-03-01 at 16.44.00.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_2ypQAU%2FScreenshot%202024-03-01%20at%2016.44.00.png)

# Data partitioning
here we will learn more about Data partitioning models together with their pos and cons

## why partition data?
data is an asset for any organisation. increasing data and concurrent read/write traffic to the data puts scalability pressure on traditional databases. as a result the latency and throughput are affected. traditional databases  are attractive due to their properties such as range queries . a range query is a common database operation that retrieves all records where some value is between an upper and lower boundary. secondary indices . a secondary index is a way to efficiently access records in a database by means of some piece of information other than the priamary key. and transactions. a transaction is a single logical unit of work that accesses and possibly modiies the contents of a database. with the ACID properties.
at some point, a single node-based database is not enough to tackle the load. we might need to distribute the data over many nodes but still export all the nice properties of relational databases. in practice, it has proved challengin to provide single-node database-like properties over distributedn database.
one solution is to move data to a NoSQL-like system. however, the historical codebase and its close cohesion with traditional databases make it an expensive problem to tackle. 
organizations might scale traditional databses by using a thord party solution. but often, integrating a third party solution has its complexities. more importantly, there are an=bundant opportunities to optimize for the specific problem at hand and get much better performance than a general-purpose solution. 
data partitioning or sharding enables us to use multiple nodes where each node manages some part of the whole data. to handle increasing query rates and data amounts, we strive fpr balanced partitions and balanced read/write load.
we will discuss different ways to partition data, related challenges, and their solutions in this lesson.
![Screenshot 2024-03-04 at 07.51.14.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_2es6WC%2FScreenshot%202024-03-04%20at%2007.51.14.png)

## Sharding
to divide load among multiple nodes, we need to partition tha data by a phenomenon called **partitioning** or **sharding**. in this appraoch, we split a large dataset into smaller chunks of data stored at different nodes on our network.
the partitioning must be balanced so that each partition receives about the same amount of data. if partitioning is unbalanced, the majority of querire will fall into a few partitions. partitions tht are heavily loaded will create a system bottleneck. the efficacy of partitioning will be harmed because a significant portion of data retrieval queries will be sent to the nodes that carry the highly congested paritions. such partitions are nown as hotspots. generally, we use the following two ways to shard the data. 
  **vertical sharding**
  **horizontal sharding**

### vertical sharding
we can put different tables in various database instances,which might be running on a different physical server. we might break a table into multiple tables so that some columns are on one table while the rest are in the other. we should be careful if there are joins between multiple tables. we may like to keep such tables together on one shard. 
often, **vertical sharding** is used to increase the speed of data retrieval from a table consisting of columns with very wide text or a binary large object(blob). in this case, the column with large text or blob is split into a different table. 
as shown below, the ```Employee```, able is divided into two table; a reduced employee table and an employeePicture table. the employeepicture table has just two columns, employeeID and picture, separated from the original table. morever, the primary key is added in both partitioned tables. this makes the data read and write easier, and the reconstruction of the table is performed efficiently. 
![Screenshot 2024-03-04 at 08.02.40.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_lWNkHz%2FScreenshot%202024-03-04%20at%2008.02.40.png)

### Horizontal sharding
at times, some tables in the databases become too big and affect read/wrote latency. **Horizontat sharding** or partitioning is used to divide a table into multiple tables by splitting data row-wise as hwon below. each partition of the original table distributed over database server is called a **shard**. there are two strateies to do the:
  * key-range based sharding
  * Hash-based sharding

### key-range based sharding
in this, each partition is assigned a continous range of keys. 
in the figure below, horizontal partitioning on the invoice table is performed using key-range based sharding with customerid as the paritioning key. the two different colored tables represents the partitions. 
![Screenshot 2024-03-04 at 08.07.28.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_OLjTqx%2FScreenshot%202024-03-04%20at%2008.07.28.png)
sometimes, a database consist of multiple tables bound by foreign key relationsips. in such a case, the hosrizontal partition is performed using the same partition key on all tables in a relation. tables or subtables that belong to the same partition ley are distributed to one database shard. the following figure shows the several tables with same partition key are placed in a single database shard.
![Screenshot 2024-03-04 at 08.10.14.png](..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2Fjd%2F_tr5km9d1bn2rtnrw8k2rxsc0000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_5e87IX%2FScreenshot%202024-03-04%20at%2008.10.14.png)

### advantages
* using key-range based sharding method, the range-query-based schema is easy to implement. we precisely know where to look for a specific range of keys. 
* range queries can be performed using the partitioning keys, and those can be kept in partitions in sorted order. hoe exactly such a sorting algorithm happens over time as new data comes in is implementation soecific
### Disadvantages
* Range queries cannot be performed using keys other than the partitioning key.
* if keys are not selected properly, some nodes may have to store more data due to an uneven distribution.


## Distributed Monitoring
* Monitoring systems are critical in distributed systems because they help in analyzing the system and alerting the stakeholders if a problem occurs.
* we can make a monitoring system scalable using a hybrid of the push and pull methods.
* Heat maps are a powerful tool for visualization and help us learn about the health of thousands of servers in a compact space.
* in a distributed system, it is difficult to detect and respond to errors on the client side. so it is necessary to monitor such events to provide a good user experience.
* we can handle errors using an independent agent that sends service reports about any failures to a collector. such collectors should be independent of the primary service in terms of infrastructure and deployment.

## The distributed Cache
we studied the basics of the cache and designed a distributed cache that has a good level of availability, high performance, high scalability, and low cost. our mechanism maintains high availability using replicas, though if all replicas are in one data center, such a scheme won't tackle full data center failures. now that we have learned about the design basics we can explore popular open-source frameworks like Memcached and Redis

## The Distributed Messaging Queue
* why is the order of messages important and how do we enforce that order?
* How does Ordering affect performance? How do we handle concurrency while accessing a queue

## Pub-sub system
* we saw two designs of pub-sub, using queues and using our custom storage optimized for writing and reading small-sized data.
* there are numerous use cases of a pub-sub. due to decoupling between producers and consumers, the system can scale dynamically, and the failures are well-contained. Additionally, dur to proper accounting of data consumption, the pub-sub is a system of choice for a large-scale system that produces enormous data. we can determine precisely which data is needed and not needed. 
















