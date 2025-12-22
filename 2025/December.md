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
