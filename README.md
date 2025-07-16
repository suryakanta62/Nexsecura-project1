# Nexsecura-project

CTF Challenge :- Solving Basic Penetration Testing machine

Hello, LinkedIn Network!

on the 2-month & 15 days of journey of cybersecurity. I am very excited to learn this machine, because this machine is less hard than other machines.
Through these challenges, we can learn new things to solve the hard machine, & how we can solve these machines as we go from easy to hard machine challenge level, & their tool we can use & learn easily.


🚩 Challenge Overview:-

 The Basic Pentesting machine is designed for beginners looking to develop core penetration testing skills. This intentionally vulnerable VM simulates a real-world environment and is great for learning how to exploit services such as SSH, SMB, and web-based applications.

🔍 Goal:-

 Gain a foothold, escalate privileges, and capture the flag(s).

🧰 Tools Used:-

1)nmap – for network scanning
2)enum4linux – for SMB enumeration

🧭 Walkthrough Summary:-

1)Reconnaissance:-
Used nmap -sC -sV to scan open ports (port 22, 139, 445, 80).

2)Enumeration:-
enum4linux revealed usernames from SMB shares.
Web service on port 80 was hosting a vulnerable login page.

3)Brute Forcing:-
Used hydra to brute-force SSH with obtained usernames.
Gained access via valid credentials.

4)Post-Exploitation:-
Explored the user environment for misconfigurations.
Found a password hash and cracked it using john.

5)Privilege Escalation:-
Checked for sudo rights or vulnerable binaries.
Escalated privileges using a writable script executed by root.

🎯 Flag Captured:-
 Successfully gained root access and captured the flag located in /root/.

📝 Key Takeaways:-

Mastering the basics of enumeration and brute-force techniques is crucial.
Always enumerate thoroughly before jumping to exploitation.
Privilege escalation often involves looking for misconfigurations or weak permissions.
Documentation and tool chaining are essential for an efficient workflow.
