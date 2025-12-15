### **December 1, 2025**

**Today's Focus**
* Solve 2 labs from eJPT training course.
* Attempt a ctf challenge on tryhackme.

**What I Learned/Did ?**
* I solved two ctf labs from eJPT training course.
* These labs were based on exploiting vulnerabilites and services like ssh, webdav, samba, shellshock.
* Escalated privileges using suid binaries.
* Attempted a lab on tryhackme, exploited sql injection using sqlmap and dumped the database.
* Database dump revealed the ssh credentials. Gained initital access using the credentials.

**Thoughts**
* Attempting the tryhackme me after so long felt refreshing. 

---

### **December 2, 2025**

**Today's Focus**
* Logged of early.

**What I Did/Learned ?**
* Revised the yesterday's topics and logged of early today.

**Thoughts**
* Didn't do anything significant today, was feeling a bit down so took time off.
---
### **December 3, 2025**

**Today's Focus**
* Solve eJPT CTF lab.

**What I Learned/Did ?**
* I solved a ctf lab, it involved exploiting microsoft sql server.
* Used msfconsole to exploit mssql.

**Thoughts**
* The mssql_payload module was buggy, wasted a lot of time in it.
---
### **December 4, 2025**
**Today's focus**
* Solve eJPT labs.

**What I Did/Learned ?**
* Solved two more labs from eJPT training material.

**Thoughts** 
* Solve a lab completely and another lab was half solved, will finish it tomorrow.
* Just knowing the version of a service can be crucial, I realized that today.
---
### **December 5, 2025**
**Today's focus**
* Solve eJPT lab.

**What I Did ?**
* I solved another ctf lab today.

**Thoughts**
* The labs are getting repetitive, I need to shift focus to labs from tryhackme or hackthebox.
---
### **December 6, 2025**
**Took time off**
---

### **December 7, 2025**
**Today's Focus**
* Research on CVE-2025-55182.

**What I Learned ?**
* I dove deep into React Components, React server components, how and why RCS is needed, how it serialized and deserializes data.
* Learnt about RCS's Flight Protocol.
* Wrote custom exploit code based on a PoC.

**Thoughts**
* This "React2Shell" vulnearbility is classified as Insecure Deserialization vulnerability.
* Wrote a python exploit for this, RSC receives it but payload is failing to execute.

---
### **December 08, 2025 - December 10, 2025**
**Took time off due to bad health.
---

### **December 11, 2025**
**Today's Focus**
* Get back into routine.
* Solve a trthackme lab.

**What I Did ?**
* Solve "Retro" ctf lab on tryhackme, it was hard in difficulty.
* Initial access was obtained via leaked credentials.
* Privilege escalation was obtained by either exploiting CVE-2019-1388 and CVE-2017-0213.

**Thoughts**
* I used the latter CVE (2017-0213) for escalation.
---
### **December 12, 2025**
**Today's Focus**
* Solve "Relevant" from tryhackme.
* Publish the entry for it in Hack Log (my collection of writeups).

**What I Did ?**
* I solve the "Relevant" lab on TryHackMe.
* The lab featured
  - Insecure access
  - Leaked credentials
  - Uploading shell via smb server for initial access
  - Using impersonation tokens to escalate to Authority\System

**Thoughts**
* Learnt something new, sometimes samba shares can also be hosted via web server, had to look a writeup for this, uploaded the reverse shell using this technique.
* The complete writeup for this available [here](https://github.com/Kugelbyte/Hack-Log/journal/2025-12-12-relevant.md)
---

### **December 13, 2025**
**Today's Focus**
* Finish the analysis report for CVE-2025-55182 (React2Shell).
* Post the report on github and linkedin.

**What I Did ?**
* Finally, finished the report, took reference from Tryhackme's lab, and the PoC provided for it.

**Thoughts**
* Link to the report : https://github.com/Kugelbyte/React2Shell-Analysis/tree/main
---
### **December 14, 2025**
**Today's Focus**
* Solve CTF lab on post-exploitation.

**What I Did ?**
* Exploited the ssh (libssh) service to gain initial access.
* Escalated privileges using improper permissions on "/etc/shadow" file.

**Thoughts**
* I confused myself with the IP address of the target, wasted some time scanning different IP.
---

### **December 15. 2025**
**Today's Focus**
* Solve two ctf labs from eJPT training.
* Solve "Blog" from tryhackme.

**What I Did ?**
* Solved the couple of labs from eJPT, based on post exploitation and web app exploitation.
* Solved Blog from tryhackme, it was based on wordpress 5.0 exploitation.

**Thoughts**
* I don't like this puzzle type labs and challenges, the more the real they are the better.
