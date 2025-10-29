### **October 27, 2025**

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

---

### **October 28, 2025**

**Today's Focus**
* Understand the context of XSS in javascript.

**What I Learned?**
* Sometimes we can just simply terminate the existing script and inject our payload. It won't work always as applications can encode '<' and '>'.
```html
<script>
var = 'value';
</script>

#.injection can happen like this below..

<script>
var = </script><script>alert(1)</script> or
var = </script><img src=1 onerror=alert(1)>
</script>
```
* In some cases the context can be inside JS string literals, in that we have to break out of that string literal,
```html
useful payloads

';alert(document.domain)
or
'-alert(document.domain)//
```
* This require some clever thinking, it's about how to introduce single quote.
* Some applications even block single quotes using a backslash before the single quote, this backslash tells the parser to parse single quote literally instead of considering it as a special character.
* To bypass this inject the single quote with a backslash
```html
\';alert(document.domain)//
this will get converted to
\\';alert(document.domain)//
```
* This works when applications fail to esacpe backslash itself.

**Thoughts**
* It is tricky to determine what payload will work.
* It's all trial and error, best way is to try and inject characters one by one and check responses, this will help in framing the payload effectively.
* Tomorrow will see some more contexts of XSS.
  
---

### **October 29, 2025**

**Today's Focus**

* XSS context in javascript template literals.
* Understanding client-side template injection.
* Grasp the understanding of content security policy.

**What I Learned ?**
* Template literals can be identified by backticks ` `.
```html
<script>

var msg = `user controlled input`;

</script>
```
* This will allow embedded javascript expression to execute.
* Here in place of template literal between ``, we can insert ${..} to embed javascript expression.
```html
<script>
var msg = `${alert(document.domain)}
</script>
```
* Content Security Policy is a browser security mechanism to prevent XSS.
* It basically works by restricting the resources that a page can load.
* If the response contains a header names "Content-Security-Policy" that means it is enabled, the header values contains policies separated by commas.

**Thoughts**
* There are techniques to bypass Content Security Policy, they seem a bit tough to understand at first.
* Really liked how a template injection works, the premise of it.

