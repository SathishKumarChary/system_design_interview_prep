## Communication

[![](https://github.com/donnemartin/system-design-primer/raw/master/images/5KeocQs.jpg)](https://github.com/donnemartin/system-design-primer/blob/master/images/5KeocQs.jpg)  
_[Source: OSI 7 layer model](http://www.escotal.com/osilayer.html)_

### Hypertext transfer protocol (HTTP)
HTTP is a method for encoding and transporting data between a client and a server. It is a request/response protocol: clients issue requests and servers issue responses with relevant content and completion status info about the request. HTTP is self-contained, allowing requests and responses to flow through many intermediate routers and servers that perform load balancing, caching, encryption, and compression.

A basic HTTP request consists of a verb (method) and a resource (endpoint). Below are common HTTP verbs:

|Verb|Description|Idempotent*|Safe|Cacheable|
|---|---|---|---|---|
|GET|Reads a resource|Yes|Yes|Yes|
|POST|Creates a resource or trigger a process that handles data|No|No|Yes if response contains freshness info|
|PUT|Creates or replace a resource|Yes|No|No|
|PATCH|Partially updates a resource|No|No|Yes if response contains freshness info|
|DELETE|Deletes a resource|Yes|No|No|

*Can be called many times without different outcomes.

HTTP is an application layer protocol relying on lower-level protocols such as **TCP** and **UDP**.

#### Source(s) and further reading: HTTP
- [What is HTTP?](https://www.nginx.com/resources/glossary/http/)
- [Difference between HTTP and TCP](https://www.quora.com/What-is-the-difference-between-HTTP-protocol-and-TCP-protocol)
- [Difference between PUT and PATCH](https://laracasts.com/discuss/channels/general-discussion/whats-the-differences-between-put-and-patch?page=1)