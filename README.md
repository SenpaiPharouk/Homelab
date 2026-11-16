**Cybersecurity Homelab**  
This repository is where I document the build of my personal  
   
 cybersecurity homelab. It covers everything from preparing my Ubuntu  
   
 host to setting up virtual machines, building isolated networks and  
   
 working through practical security exercises.  
I'm building this to learn by doing, and to keep a clear record of what  
   
 I did, what went wrong and how I fixed it. If you are building something  
   
 similar, I hope the notes save you some time.  
**What this project is about**  
The lab is a safe, controlled environment where I can build  
   
 infrastructure, try out security tools, look at network traffic and  
   
 practise authorised security assessments without touching any real  
   
 systems.  
My goals are to:  
- Set up a virtualised cybersecurity lab on my own machine  
- Install and configure Kali Linux as my attacker machine  
- Build isolated virtual networks so nothing I test can reach my home  
   
 network  
- Deploy deliberately vulnerable machines to practise against  
**Tools used**  
- Host operating system: Ubuntu Linux  
- Virtualisation: VirtualBox  
- Security operating system: Kali Linux  
- Version control: Git and GitHub  
**My setup**  
- Host CPU: Intel(R) Core(TM) i5-7300U (4) @ 3.50 GHz  
- Host RAM: 5.30 GiB used / 7.13 GiB total (74%)  
- Host storage: 76.21 GiB used / 126.90 GiB total (60%) — ext4  
- Hypervisor: VirtualBox  
Virtual machines:  
- Kali Linux: attacker machine, installed from the official installer  
   
 ISO  
- Target machine: Metasploitable  
A network diagram will go in docs/network-architecture.md once the  
   
 network is built.  
**How the repository is organised**  
- docs/ holds the architecture, setup guides and technical  
   
 documentation  
- virtual-machines/ holds a build record for each virtual machine  
- practical-labs/ holds one folder per lab, each with its own write-up  
- screenshots/ holds the images used in the documentation  
- scripts/ holds scripts and configuration files used in the lab  
- notes/ holds my own references, cheat sheets and troubleshooting  
   
 notes  
Each lab write-up follows the same format: objective, environment,  
   
 steps, findings and lessons learned.  
**Security disclaimer**  
Everything in this repository is done inside an isolated lab I control,  
   
 Please do not use anything here against systems you do not own or have  
   
 written permission to test.  
**About me**  
I'm SenpaiPharouk, a cybersecurity Enthusiast I am building and  
   
 documenting things in the open.  
GitHub: [https://github.com/SenpaiPharouk](https://github.com/SenpaiPharouk "https://github.com/SenpaiPharouk")  
