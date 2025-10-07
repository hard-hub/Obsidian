- What is CORS.?
- What is an Origin.?
- What is the problem that CORS solves.?
- Why do you need to use CORS.?
- What happens if we don't use CORS.?
- How does CORS actually work in the behind the scenes.?
- Where can and should you use CORS.?
- When should you use CORS.?
- What is `Access-Control-Allow-Origin`.?
- What is `*`.?
- When can we not use `*` in `Access-Control-Allow-Origin`.?
- What is **Preflight Request**.?
- CORS is a browser-to-server feature, hence when you use Postman, it wouldn't reflect the CORS issue as it is a server-to-server communication.
- What is an `OPTIONS` Request.?
- What is SOP[Same Origin Policy].?
- How was and when was the issue of SOP found and it was resolved using CORS.?
- Are CORS request and HTTP request same or different.?
- Simple[GET, POST, HEAD, Normal Content Type, No Header] & Non-Standard[PUT, PATCH, DELETE] CORS requests.?
- *If you can't modify the backend, you can use `Proxy` to forward request to the same origin, this makes the request appear as if they are coming from the same origin.*
- 


### XSS
- What is XSS.?
- How is it implemented.?
- Three Types of XSS attacks : **Stored XSS** && **Reflected XSS** && **DOM-Based XSS**
- How can you solve this attack and prevent it from happening.?
- *Escape HTML Characters && Sanitize input using security libraries.*
- What is DOM Purify.?
- *Use CSP headers to block inline scripts.*
- **DOM-Based XSS** --> The Invisible Java-Script Based Attack
- *You use `textContent` instead of `innerHTML`.*

### SQL Injection
- What is SQL Injection.?
- How to prevent it.?
- How does one implement SQL Injection.?
- *Always Use Prepared Statements or Parameterized Queries.*
- How to use Prepared Statements.?
- *Escape User Input.*
- *Limit Database Privileges*
- *Use a Web Application Firewall.[WAFs]*
- *Monitor Logs for Suspicious Activity.*

### CSRF 
- What is CSRF.?
