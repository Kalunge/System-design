# URL Shortener
Let us design a URL, similar to services like [Bitly](https://bitly.com/), [TinyUrl](https://tinyurl.com/app)

## What is a URL Shortener
a URL shortener service creates an alias or a short URL for a long URL. Users are redirected to the original URL when they visit these short links

## Why do we need a URL Shortener
    saves space in genera when we are sharing a URL;
    Users are less likely to mistype a shorter URL
    we can optimize links across devices, allowing us to track individual links
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
similarly, for the read requests, since we expect












                











