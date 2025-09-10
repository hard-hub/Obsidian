### Ways to increase your API performance
- *Optimization should not be the first step in your process.* Why so.? What should be the first step then.?
- *The first step should always be to identify the actual bottlenecks.* What do you mean by that.? How to do it.?
- **CACHING**
- **CONNECTION POOL**
- What are `Serverless architectures`.?
- *AWS RDS Proxy && Azure SQL Database Serverless*. What are these.?
- **AVOID (N+1) QUERY PROBLEMS**
- **PAGINATION**
- **LIGHTWEIGHT JSON SERIALIZATION**
- **COMPRESSION**
- What is `Brotli`.?
- **ASYNCHRONOUS LOGGING**


### Tips for API Design
- **USE CLEAR NAMING**
- **ENSURE RELIABILITY THROUGH IDEMPOTENT APIs**
- GET, PUT & DELETE are Idempotent, while POST & PATCH aren't. Idempotence mainly means that when you call a certain http method, the response should always be the same and not to create new response each and every time if a same request is provided.
- **ADD VERSIONING**
- **ADD PAGINATION**
- **USE CLEAR QUERY STRINGS FOR SORTING AND FILTERING API DATA**
- **DONT MAKE SECURITY AN AFTERTHOUGH WHEN DESIGNING APIs**
- **KEEP CROSS RESOURCE REFERENCES SIMPLE**
- **PLAN FOR RATE LIMITING**
---
- **USE HTTP METHODS CORRECTLY**
- **USE NOUNS FOR RESOURCES IN YOUR URLs or URIs**
- **USE APPROPRIATE STATUS CODES**
- **ERROR HANDLING**
- **VALIDATE REQUESTS**
- **VERSIONING**
- **PAGINATION, FILTERING & SORTING**
- **HATEOAS** >> Hypermedia As The Engine Of Application State
- **SECURITY**
- [ ] Understand Security Basics to configure into APIs ⏳ 2025-08-14 📅 2025-08-15
---


### Logging Practices
- What is `Logging`.?
- What are Log Levels.?
	- **INFO**
	- **WARN**
	- **ERROR**
	- **FATAL**
- What is `Structured Logging`.?
- *Logging Libraries in C#*
- What to capture in Logging.? How much.?
- What is `Telemetry`.?
### API Architecture Styles
- **SOAP** >> Xml-based for enterprise application
- **RESTful** >> Resource-based for web servers
- **GraphQL** >> Query language reduce network load
- **gRPC** >> High performance for Microservices
- **WebSocket** >> Bi-directional for low latency data exchange
- **Webhook** >> Asynchronous for event-driven application
- *What is **Richardson Maturity Model**.?*
- *What is **Rate Limit**.?*
- *What is **Token Bucket Algorithm**.?*


