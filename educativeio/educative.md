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





























