
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


### **January 06, 2025**

* Resumed the testing on GraphQL end-point.
* I tried using "graphw00f" to fingerprint the GraphQL engine but it didn't worked.
* Tried enumerating the schema but introspection is disabled.
* The json structure of the query fetching user details is like this:
  ```gql
  [{"operationName":"Me","variables":{},"query":"query Me {\n  me {\n    id\n    legacyId\n    email\n    firstName\n    lastName\n    avatarUrl\n    birthDate\n    gender\n    hasPassword\n    phone\n    totalYumsEarned\n    totalYumsBurned\n    totalReservation\n    hasBookmark\n    hasReservation\n    createdAt\n    hasCompletedBookmarksOnboarding\n    highestEligibleDiscountCode {\n      amount {\n        currency {\n          decimalPosition\n          isoCurrency\n          __typename\n        }\n        value\n        __typename\n      }\n      __typename\n    }\n    gamification {\n      name\n      __typename\n    }\n    giftCards {\n      id\n      status\n      __typename\n    }\n    phoneConfirmed\n    stats {\n      segment\n      __typename\n    }\n    __typename\n  }\n  connectionStatus\n  customerOptIn {\n    id\n    optIn {\n      id: optInId\n      optInId\n      type\n      active\n      status\n      __typename\n    }\n    __typename\n  }\n}"}]
  ```
* Also the GraphQL recommendation is disabled, inputting wrong field names resulted in 400 Bad Request and "GRAPHQL_VALIDATION_FAILED" error in response.
* I tried editing the query, tested whether if injecting the "id" in "variables" fetch the user details, but the server ignored it.
* This meant that server isn't using "id" to fetch details, rather it was using JWT token to fetch details.
* Also when I observed the JWT token payload
```json
{
    "roles": [
        "identified",
        "authenticated"
    ],
    "user": {
        "type": "customer",
        "id": "d57d2601-019f-45c0-a861-788728f3c80d"
    },
    "sessionId": "************",
    "iat": 1767700163,
    "exp": 1767700463,
    "iss": "************",
    "sub": "session",
    "jti": "************"
}
```
* The "id" field had the same value as the "id" of the user, I logged out and logged in but the "id" in JWT token remained same, this might suggest:
  - During account creation, server created an unique "id" for my account alongwith storing other information like email and password.
  - Then for each login session while creating the token, it assigns the unique "id" to the JWT's "id".
 
---
### **January 07, 2025**

* The observation I made about JWT token yesterday, it seems that it is standard behavior in the web applications.
* I tried testing whether if I can manipulate JWT itself.
* Tested with putting "alg:NOne" and similar variants to see if it works, it didn't.
* Tested removing the signature from the token, it didn't worked.
* I observed another behavior that sometimes the application asks for an OTP if it fails to recognize the device (maybe it logs the MAC of the device to create a fingerprint and associate it with the account).
* The request was like this:
```gql
  [{"operationName":"GenerateTotp","variables":{"input":{"customerUuid":"3b8f0946-da72-4df9-a35a-d38a24f4831a","requestType":"DINER_CONNECTION"}},"query":"mutation GenerateTotp($input: GenerateTotpInput!) {\n  generateTotp(input: $input)\n}"}]
```
* It is taking that "customerUuid" field. 
* Assuming this user as B, I made the request from user A's account with keeping B's uuid in "customerUuid" field and it did generated a code, and the code arrived in A's mail.
---

