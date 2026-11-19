# Cybersecurity Homelab

Welcome to my **Cybersecurity Homelab** repository!

This repository documents the process of building my personal cybersecurity lab, from preparing my Ubuntu host machine to configuring virtual machines, creating isolated networks, and performing hands-on security exercises.

I'm building this homelab to develop practical cybersecurity skills and document the projects I complete along the way. I'll be sharing what I build, the tools I use, the challenges I encounter, and how I troubleshoot and solve problems.

If you're also learning cybersecurity or building your own homelab, I hope my documentation can help you along the way.

## What This Project Is About

The goal of this project is to create a safe, controlled environment where I can explore and practise cybersecurity concepts without targeting real-world systems.

Through this homelab, I aim to:

- Build a virtualised cybersecurity lab on my personal computer.
- Install and configure Kali Linux as my attacker machine.
- Deploy deliberately vulnerable virtual machines for practice (Metasploitable).
- Configure isolated virtual networks for controlled testing.
- Learn network scanning and reconnaissance using **Nmap**.
- Explore vulnerability assessment and exploitation using **Metasploit**.
- Analyse network traffic and packets using **Wireshark**.
- Perform web application security testing using **Burp Suite**.
- Explore wireless network security and auditing using **Aircrack-ng**.
- Complete simulated penetration testing projects and document the findings.

## Tools and Technologies

| Component | Technology |
|---|---|
| Host Operating System | Ubuntu Linux |
| Virtualisation | Oracle VirtualBox |
| Security Operating System | Kali Linux |
| Target Machine | Metasploitable |
| Network Scanning | Nmap |
| Exploitation Framework | Metasploit |
| Network Analysis | Wireshark |
| Web Application Security | Burp Suite |
| Wireless Security Auditing | Aircrack-ng |
| Version Control | Git and GitHub |

## My Homelab Setup

**Host Machine**

- CPU: Intel Core i5-7300U (4 cores)
- RAM: 7.13 GiB total
- Storage: 126.90 GiB total
- Filesystem: ext4

**Virtual Machines**

- **Kali Linux:** My attacker machine, installed using the official Kali Linux installer ISO.
- **Metasploitable:** My deliberately vulnerable target machine for practising security assessments.

A network architecture diagram will be added to `docs/network-architecture.md` once the lab network has been configured.

## Repository Structure

The repository is organised to keep the project documentation clear and easy to navigate.

- `docs/` — Network architecture, setup guides, and technical documentation.
- `virtual-machines/` — Build and configuration records for each virtual machine.
- `practical-labs/` — Hands-on exercises, organised into individual lab folders.
- `screenshots/` — Screenshots supporting the documentation.
- `scripts/` — Scripts and configuration files used in the lab.
- `notes/` — Personal references, cheat sheets, and troubleshooting notes.

Each practical lab will follow a consistent documentation format:

1. Objective
2. Lab environment
3. Tools and commands used
4. Step-by-step procedure
5. Findings and observations
6. Lessons learned

## Security Disclaimer

All practical exercises documented in this repository are intended for use within my own controlled lab environment.

The tools and techniques demonstrated here are for educational purposes only. Do not use them against systems, networks, or devices without proper ownership or explicit authorisation.

## About Me

I'm **SenpaiPharouk**, a cybersecurity enthusiast documenting my journey into the world of cybersecurity through hands-on learning and practical projects.

I'm learning, experimenting, making mistakes, solving problems, and sharing my progress openly.

**GitHub:** [@SenpaiPharouk](https://github.com/SenpaiPharouk)

---

*Learning by doing. Building skills one lab at a time.*
