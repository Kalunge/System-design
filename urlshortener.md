# URL Shortener
Let us design a URL, similar to services like [Bitly](https://bitly.com/), [TinyUrl](https://tinyurl.com/app)

## What is a URL Shortener
a URL shortener service creates an alias or a short URL for a long URL. Users are redirected to the original URL when they visit these short links

## Why do we need a URL Shortener
* saves space in genera when we are sharing a URL;
* Users are less likely to mistype a shorter URL
* we can optimize links across devices, allowing us to track individual links
## Requirements
A URL shortening service should meet the following requirements
### functional Requirements
- given a URL, our service should generate a shorter and unique alias for it
- users should be redirected to the original URL when they visit the short Link.
- links should expire after a default lifespan

### Non-functional Requirements   
- High availability with minimal latency
- The system should be scalable and efficient


### Extended Requirements   
- Prevent abuse of service
- Record analytics and metrics for redirections  
## Estimation and Constraints
let us start with the estimations and constraints
PRO TIP -> make sure to check any scale or traffic related assumptions with your interviewer

### Traffic
THis will be a read-heavy system, so let us assume a  100:1  read/write ratio with 100 million links generated per month

#### Reads/Writes per month

for reads per month

       100 * 100 million = 10 billion / month

for writes per month  

        1 * 100 million = 1000 million / month

#### What would be Requests per second for our system
100 million requests per month translates into 40 requests per second
        
         100 million / (30 days * 24 hrs * 3600 seconds) = ~ 40 urls / second
and with 100:1 read/write ratio, the number of redirections will be

        100 * 40 URLS/second = 4000 requests / second

#### Bandwidth
since we expect about 40 URLs every second, and if we assume each request is of size 500 bytes then the total incoming data for the write requests would be
        
        40 * 500 bytes = 20 KB / second
similarly, for the read requests, since we expect   about 4K redirections, the total outgoing data would be
        
        4000 URLS / second * 500 bytes = ~ 2 MB / second

#### Storage
 for storage, we will assume we store each link or record in our database for 10 years. Since we expect around 100 million new requests every month, the total number of records we will need to store would be 
        
        100 million * 10 years * 12 months = 12 billion  URLs

Like earlier, if we assume each stored record will be approximately 500 bytes. we will need around 6TB of storage
        
        12 billion *  500 bytes = 6 TB
#### Cache
for caching, we will follow the classic [pareto principle ](https://en.wikipedia.org/wiki/Pareto_principle) also known as the 80/20 rule. this means that 80% of the requests are for 20% of the data, so we can cache around 20% of our requests
since we get around 4K read or redirection requests each second.this translates into 350M requests per day.

        4000 URLs / second * 24 Hrs * 3600 seconds = ~350 millio r. 

this means we will need around 35 GB of memory per day
        
        20 percent * 350 Million * 500 bytes = 35 GB / per day

 #### High Level Estimates
| Type                | Estimate     |
|---------------------|--------------|
| Writes(new URLs)    | 40/s         | 
| Reads(Redirection)  | 4K/s         |
| Bandwidth(Incoming) | 20 Kb/s      |    
| Bandwidth(Outgoing) | 2 MB/s       |    
| Storage(10 Yrs)     | 6 TB         |    
| Memory(Caching)     | 350 GB / Day |    
 
## Data Model Design
next we will focus on the data model design. Here s our database schema

``` mermaid
erDiagram
    users {
        uuid id
        string name
        string email
        timestamp createdAt
    }
    urls {
        string hash
        uuid userID
        string originalURL
        string expiration
        indexes hash 
    }    
                
    users ||--|{ urls : "Has"
```
initially we can get started with just two tables.

#### users
Stores user's details sucha as ``` name, email, createdAt,``` etc

#### urls  
Contains the new short URL's properties such as ```expration, hash, originalURL, userId``` of the user who created the short URL. we can also use the hash column as an index to improve the query performance.

### What kind of database should we use
Since the data is not strongly relational, NoSQL databases such as ```Amazon DynamoDB, Apache Cassandra, MongoDB``` will be a better choice here, if we do decide to use an SQL database then we can use something like Azure SQL Database, or Amazon RDS

## API Design
let us do a basic API design for our services.

### create URL
This API should create a new short URL in our system given an original URL.

```java 
createURL(apiKey: String, originalURL: string, expiration?: Date) : String
```
#### Parameters
- API Key (```string ```): API Key provided by the user
- Original URL(```string ```): Original URL to be shortened
- Expiration(```Date ```): Expiration Date of the new URL(optional)

#### Returns
Short URL ( ```string ```) : New shortened URL



           



















