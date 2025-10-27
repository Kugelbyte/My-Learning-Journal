### **October 28, 2025: Day 1**

**Today's Focus**
* Understand the different contexts of cross-site scripting.

**What I Learned ?**
* A context in XSS basically means where the attacker controlled values appears in the response or if any validation/operation is being performed on that value by the application.
* Identifying context is crucial as it greatly helps in deciding the payload to trigger execution of javascript. Inject a alphanumeric string as value and check where it gets reflected ( inspect the page)
* I learned about the XSS in HTML tags. I am using PortSwigger's Web Security Academy as a resource.
* If the context of XSS is inside an HTML tag then we can trigger JS by either using a simple "<script></script>", this "script" tag will be inside the overlying tag.
* XSS can happen in HTML tag attributes, usually we have to escape that tag attribute and inject.

**Thoughts**
* Identifying where the value is being reflected is very crucial, it makes it easier to understand what to do next.
* After indentifying context, need to find a working payload, (this requires researching tags and their attributes).
* Tomorrow I will see XSS in javascript, this is seems a bit tough, could be, i will see it tomorrow. 

