
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
### **Janaury 3, 2026**
* Attempted a challenge on tryhackme today.
* The challenge was 'Year of the Rabbit', I didn't like it.
* This lab was very puzzle like, no where near like a simulated penetration test, involved solving puzzles instead of exploitation.
* Attempted another challenge, 'Opacity', this was way better.
* Exploited the arbitrary file upload vulnerability to upload a reverse shell.
* Obtained a keepass hash file, and cracked the hash.
---

### **January 4, 2026**
* Continued with the 'Opacity' lab.
* After cracking the keepass hash, obtained the credentials for the user 'sysadmin'.
* Obtained first flag from sysadmin's home directory.
---
### **January 5, 2026**
* Shifted focus back to my security research on the GraphQL target.
* Learnt about the basics of GraphQL (types, query, mutation, schema).
* Types define the primitive data types such as integer, string, boolean and id. They are called scalar types.
  ```gql
  type Users{
        id: ID!
        name: String!
        email: String!
        isAdmin: Boolean!
   }
  ```
* Then there area object types which are a collection of fields (query, mutation, subscription)
  - Query reads the data 
  ```gql
  query {
     Users {
              id
              name
           }
        }
  ```
  - Mutations are used to modify (update,delete) the data. Mutations have to be defined first and then they can be used to create, update or delete.
  ```gql
  mutation {
          createUser(name: 'Bob', email:'bob@mail.com){
              name
              email
  }
  }
  ```
* Schema defines the entire content (types, mutations, subscriptions).
---
