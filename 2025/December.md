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
**Took time off due to bad health.**
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
---
### **December 16, 2025**
**Today's Focus**
* Attempt "Vulnnet:Internal" on tryhackme.

**What I Did ?**
* Today I struggled with the lab on tryhackme.
* mounted shares, read config files and found redis password.
* found rsync password in redis db.

**Thoughts**
* Got frustrated so packing up for today, will do it again tomorrow.
---

### **December 17, 2025**
**Today's Focus**
* Complete yesterday's lab.
* Gain knowledge about pivoting by solving tasks on "Wreath" network in Tryhackme.

**What I Learned/Did ?**
* Completed the ctf lab from yesterday, gained root via port forwarding TeamCity service and escalating privileges.
* Spinned up the wreath network.
* Compromised a public facing linux server.
* Discovered the other hosts in the internal network by transferring nmap compiled binary to the compromised linux server.
* Successfully forwarded the http service running on the internal host to the local system.

**Thoughts**
* There are many ways to port forward (proxychains,socat,chisel).
* Yesterday's lab was had some serious problem, every few minutes i became unreachable causing me to do everything from scratch as resetting it only worked.
---

### **December 18, 2025**
**Today's Focus**
* Attempt a simulated penetration test on Tryhackme lab called Internal.

**What I Did ?**
* Did a penetration of a test environment.
* Brute forced the credentials for the wordpress admin panel.
* Uploaded a reverse shell by editing the wordpress theme template.
* Found a note in the target machine which revealed a Jenkins service running on an another machine in the internal network.
* Port forwarded the jenkins service to the local machine.
* Bruteforced the Jenkins panel credentials.
* Uploaded a reverse shell on Jenkins Script panel and successfully pivoted to another machine on the internal network.
* Found credentials for root user and gained root shell.

**Thoughts**
* This simulated lab was very good, felt very real.
---

### **December 19, 2025**
**Took the day off**

---

### **December 20, 2025**
**Today's Focus**
* Install the SSD in the SSD-Enclosure.
* Partition the SSD and install Kali Linux.

**What I Did ?**
* I installed the ssd on the enclosure, applied thermal pad on ssd, then attached it to enclosure.
* Then prepared Kali installer image via USB.
* Partitioned the disk and installed kali on ssd using the installer image on usb.

**Thoughts**
* The first boot failed and crashed, I panicked and rebooted again and Kali successfully booted.
---
### **December 21, 2025**
**Took a day off**
---

### **December 22, 2025**
**Today's Focus**
* Revise topics for eJPT exams.

**What I Did ?**
* Went through techniques for enumerating wordpress and drupal.
* Revised privilege escalation techniques.
---
### **December 23, 2025**
**Today's Focus**
* Attempt eJPT test.

**What I Did ?**
* After more than a month of preparation, I decided to attempt the eJPT test today.
* I started the test at 2 PM.
* Finished the test by 11 PM with 91% score.

**Thoughts**
* First goal accomplished, now towards my next goal!!.
---

### **December 24, 2025**
**Took a day off, much needed rest after the 9 hours long test session of yesterday.**
---

### **December 25, 2025**
**Today's Focus**
* Curate the resume, add keywords and re-formulate the sections in the resume.

**What I Did ?**
* Reformatted the differenct sections in the resume.
* Reworked on the contents of the resume, updated them with my current skills.

**Thoughts**
* Resume looks much cleaner now, need to the same with LinkedIn profile.

---
### **December 26, 2025**
**Today's Focus**
* Resume efforts on web application security.
* Revisit sql injection

**What I Learned ?**
* Solved Portswigger Academy labs on Blind SQL Injection.
* The labs focused on injection in the cookie parameter.
* In blind sql injection, there is no clear response received via HTTP of the results of the sql query or any errors.
* Blind SQLi can be exploited by triggering conditional responses
  ```SQL
  xyz' AND '1'='1    #(this will evaluate as true)
  xyz' AND '1'='2    #(this will evaluate as false) some content of the web page might change as there is no clear HTTP response, so better to observe everything carefully
  ```
* Conditional responses can also be used deduce passwords
  ```SQL
  xyz' AND (SELECT 'a' FROM users WHERE username='administrator' AND LENGTH(password) > 1)='a  #This can be used to determined length of the password by hit and try
  xyz' AND SUBSTRING((SELECT password FROM users WHERE username='administrator'),1,1)='a       #Iterating on values like a,b,c,d,... and modifying SUBSTRING function for character positions
  ```

**Thoughts**
* Since there is no clear HTTP response carried out for whether the query was success or not, it is important to observe the behavior of the application.
* The application may behave differently based on incorrect queries and correct queries (Pop-ups in web pages, changes in web pages etc)
---
### **December 27, 2025**

**Today's Focus**
* Finalize the custom tool project idea.

**What I Did ?**
* I decided to make a custom tool for fetching old urls from web archive.
* Implemented the functions to fetch archive data and filter urls.

**Thoughts**
* I am having problems in creating regex expressions to filter meaningful urls.
* Apparently the archive urls also contain bogus payloads from scanner tools and scrapers, need to filter them out too.
---
### **December 28, 2025**
**Went out for a family trip**
---
### **December 29, 2025**
**Took rest**
---

### **December 30, 2025**
**Today's Focus**
* Learn about error-based sql injection.
* Learn about time based sql injection.

**What I Learned ?**
* I learned about how to leak information by inducing errors.
```sql
#suppose a query is like
SELECT column1 FROM table1 WHERE TrackingID='';
# The CAST function is used for converting data-types and some data can be leaked by inducing an error
TrackingId=' AND CAST ((SELECT username FROM users WHERE username='administrator') AS int)--
# Data could be reflected in the error message
```
* Sometimes the application might process every query and the errors in such a way that nothing gets reflected in the responses or in the behavior of the application.
* In this case time based sql injection can be used to delay the response of the query which confirms the injection taking place.
```sql
TrackingId=1234cyz'%3BSELECT+CASE+WHEN+(1=1)+THEN+pg_sleep(10)+ELSE+pg_sleep(0)+END--
```
* If there is a delay of 10 seconds in the response, the injection took place successfully.
---
