
###  **January 1, 2026**

* Read about IDOR hunting techniques from the blog posted in Intigriti.
* The blog mentioned techniques like:
  - HTTP parameter pollution.
  - JSON globbing ( modifying json fields with unintended values such as negative integers, asterisk ).
* If the application uses UUIDs, then querying specific api endpoints like:
  - /api/v1/users/all
  - /api/v1/users/list
  - /api/v1/users
  - might reveal valid UUIDs for some entities.
* Read writeups of other hunters who found IDORs.

---

### **January 2, 2026**

* Tested the IDOR hunting techniques on a valid bug bounty target.
* I first mapped out the authentication and restaurant booking functionalities of the application.
* This particular application uses GraphQL.
* I found that a user is assigned a unique UUID (which renders traditional IDOR hunting via numerical ids ineffective).
* In some requests a field named "legacyId" is being returned in response. The value is numerical. This field might be used before devs switched to using UUIDs (therefore named as leagacy).
* Ran some checks to see if the server still uses this "legacyId" to identify users but the GraphQL is very strict.

---
