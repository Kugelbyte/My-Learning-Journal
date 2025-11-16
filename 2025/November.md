### **November 1, 2025**

**Today's Focus**
* Refresh the basics of dns recon.

**What I Learned?**
* Completed some training material on dns reconnaissance in eJPT Training course.
* Got to know about Netcraft, another dns recon utility.

**Thoughts**
* Learned about "dnsdumpster", this really provides information in comprehensive manner.
---

### **November 2. 2025**

**Today's Focus**
* Create a video for youtube and create my channel.

**What I Learned?**
* My video's theme was about a CTF Minmap to help beginners.
* Whole day went into creating a mindmap, then creating the script, editing the video and creating the channel.

**Thoughts**
* Content creation is not easy as it seems, huge respect to content creators.
* I went through my script a lot, rehearsed multiple times but then realized it is much more easier for me to have a conversation style of video rather than a pre-decided script.
* Discarded the script and recorded the video assuming that I was explaining to my younger self.
* Video is ready and scheduled to launch tomorrow November 3, 2025, it's not flawless but at least I tried and I will improve in further videos.
--- 
### **November 3, 2025**

**Today's Focus**
* Complete Information Gathering module of the eJPT training.

**What I Learned?** 
* Watched videos using Google Dorks for passive information gathering.
* Brushed up my knowledge on nmap and its different options.

**Thoughts**
* Google Dorks are really really good, I should start using them, they reveal a lot of information.
---
### **November 4, 2025**

**Today's Focus**
* Attempt the Information Gathering lab of eJPT training material.
* Active recon in the VDP target.

**What I Learned/Did ?**
* The information gathering lab of the eJPT training module consists 5 objectives/flags, I found 4 of them, only 1 flag remains.
* Did some active recon again on VDP, this time I created an account on the target and tried for bypassing access controls, trying for IDORs.
* The target's security is robust they are implementing random GUIDs instead of usernames, multiple API calls are also involved. This is not going to be easy.

**Thoughts**
* I am slowly getting that feeling of "what if i do this?" while doing active recon on VDP target.
* There are still knowledge gaps which are preventing me from seeing the bigger picture, i need to address this by learning more concepts.

---

### **November 05, 2025**

**Today's Focus**
* Continue with eJPT training.
* Learn more topics related to web security.

**What I Learned ?**
* Watched some eJPT training material on OSI model and nmap, I was already familiar with OSI model so breezed through that part.
* Learned some host discovery techniques in nmap and when to use them.
* After 12 PM started feeling drowsy and headache started so canceled the web security topics and instead read vulnerability disclosure reports by other bug hunters.

**Thoughts**
* I need to keep pushing everyday, that is the only way I am going to make it, only action can save me.
* After reading the reports of other hunters, I realized the techniques they used were not advanced and nothing out of my knowledgebase.
* I felt a bit hopeful, I will find the bug one day, just a matter of time.
--- 

### **November 06, 2025**

**Today' Focus**
* Cover more nmap concepts from eJPT training.
* Learn concepts from Portswigger Academy.

**What I Learned / Did ?**
* Explored various types of scans in nmap and when to use them, such as SYN scan, ACK scan.
* Read some basic information on JWT authentication.
* Read some more reports of other hunters on SQLi.

**Thoughts**
* Today I felt a loss of energy in noon so pivoted to some report reading.
* SQL injections mentioned in those reports were found simply by running sqlmap, this gives me hope that it's not that difficult, I need to be thorough on my concepts.
---

### **November 07, 2025**

**Today's Focus**
* Explore nmap scripting engine from eJPT training material and firewall/IDS evasion techniques.
* Setup Kali Linux on Windows Subsystem for Linux (WSL).

**What I Did ?**
* Learned about nmap scripting engine and various types of scripts used for enumeration/information gathering.
* Learned about different options in nmap which can be used for firewall and IDS evasion such as fragmentation, delaying the packets.
* Set up Kali Linux on WSL and configured Kex (Kali Linux GUI for WSL).

**Thoughts**
* Although I am already experienced with nmap but today i delved into some advanced topics (firewall evasion) which was great.
* Setting up Kali on WSL took longer than expected (took my whole second half of the day).
* Finally Kali is running smooth and lag free contrary to Kali VM, I hope this will increase my productivity from now on as that horrible lag on kali vm really used to annoy me.
---
### **November 08, 2025**

**Today's Focus**
* Try to solve a challenge from hackthebox.
* Record video for youtube.

**What I Did ?**
* Started the day with jumping into hackthebox, picked up a challenge.
* This challenge introduced  me to a new concept, XLST Injection.
* I wasn't able to solve the challenge as I lacked the necessary knowledge, but i will delve more into XLST injection and attempt the challenge later.
* Recorded a video on ffuf, I did a simple demonstration of tool, showing how to fuzz and filter out results.

**Thoughts**
* XLST Injection doesn't seemed that complicated but I think I need to have a thorough understanding of XML and XXE Injection atleast at basic level.
* This time I recorded the video in parts and then combined it into whole.
---

### **November 09, 2025**

**Today's Focus**
* Upload the video to youtube.
* Watch a video from eJPT training material.

**What I Did ?**
* Uploaded the video recorded yesterday on youtube.
* Watched a video on how to output the nmap scan results in text files.

**Thoughts**
* Going to Indore tonight, tomorrow I will try to explore to new OWASP 2025.
---
### **November 10, 2025**

**Today's Focus**
* 
**What I Did ?**
* 
**Thoughts**
* Due to me being out of home, was not able to do productive learning today.

---

### **November 11, 2025**

** Today's Focus
*
**What I Did ?**
* 

**Thoughts**
* Took my time off to rest and recover from the travel fatigue, will jump back to action from tomorrow.
---

### **November 12, 2025**

**Today's Focus**
* Explore more about authentication mechanisms (session and token based).
* Learn about weaknesses in JWT.
* eJPT training material.
* Check the new OWASP Top 10 2025.

**What I Learned/Did ?**
* Refreshed my knowledge on the authentication basics.
* Learnt about the structure of JWT and the components (header, payload, signature).
```json
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiYWRtaW4iOnRydWUsImlhdCI6MTUxNjIzOTAyMn0.KMUFsIDTnFmyG3nMiGM6H9FNFUROf3wh7SmqJp-QV30

JWT is base64 encoded.
"." is used to delimit the components of the JWT token.
header.payload.signature

Header
{
  "alg": "HS256",
  "typ": "JWT"
}
Payload
{
  "exp": 1485140984,
  "iat": 1485137384,
  "iss": "acme.com",
  "sub": "29ac0c18-0b4a-42cf-82fc-03d570318a1d",
  "applicationId": "79103734-97ab-4d1a-af37-e006d05d2952",
  "roles": []
}

```
* Delved into some misconfigs in JWT implementations which can be harmful such as header and payload manipulation and bypassing signature and "alg".
* Watched eJPT training material on how to import nmap results to metasploit.
* Browsed the new categories introduced in OWASP Top 10 2025.

**Thoughts**
* JWT tokens are widely used in authentication, they are robust in nature but the problems arises from their insecure implementation by developers.
* OWASP Top 10 has been updated after 4 years, Broken Access Control still tops the list.
---
### **November 13, 2025**

**Today's Focus**
* Learn about more JWT attack techniques.
* Solve labs on JWT attacks.
* Learn about auxiliary modules in metapsloit (eJPT training).

**What I Learned ?**
* Explored more attack vectors in JWT, particularly header parameter injections (using jwk,jku,kid).
* Injecting self signed JWTs via jwk parameter.
* Injecting self signed JWTs using jku parameter.
```json

{
    "kid": "../../path/to/file", 
    "typ": "JWT",
    "alg": "HS256",
    "k": "asGsADas3421-dfh9DGN-AFDFDbasfd8-anfjkvc"
}
```
* Solved the labs on how to exploit header parameter injections.
* Learnt about enumerating services (ftp,smb) using auxiliary modules in metasploit.

**Thoughts**
* The JWT attack techniques which I explored today were very good, the flaw isn't in JWT but in it's implementation by the developers and developers can get very careless.
* Really enjoyed the Portswigger labs on the JWT attacks.
* Although I was already familiar with enumeration via auxiliary modules in metasploit but the training material gave a really good refresher on it in a structured way.

---

### **November 14, 2025**

**Today's Focus**
* Revise JWT attacks.
* Do some active Reconnaissance.

**What I Did ?**
* Revisited the JWT attacks.
* Did some active Reconnaissance.

**Thoughts**

* Day was average,didn't felt the desire to do much so did some revision.
* Going to Katangi tonight for weekend.

---
### **November 15, 2025**

**Today's Focus**
* Configure Proton VPN on Kali Linux (WSL).

**What I Did ?**
* Configured proton vpn via openvpn as desktop client installation was corrupted.
* The "apt" package installer was failing again and again in installing proton vpn, tried many ways to troubleshoot it, none worked.
* In the end, had to download openvpn client files for the proton vpn, this solution worked.

**Thoughts**
* apt utility caused a headache, it was not recognising proton repo and repository was somehow not getting added in sources.list.
* Finally found a workaround by using openvpn, it is not convenient but it works.

---

### **November 16, 2025**

**Today's Focus**
* Practice nmap scans on some targets.
* Learn shodan query fundamentals.

**What I Did/Learned ?**
* Ran some nmap commands in on the targets to keep the knowledge fresh.
* Read about how to make queries in shodan
```json
country: in
product: mysql
org: "XYZ Corporation"
```
**Thoughts**
* Shodan is a great resource for finding a plethora of targets. 
