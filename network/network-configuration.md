**Network Configuration -- Isolated Network**  
To ensure a safe testing environment, I configured an isolated network  
   
 in Oracle VirtualBox for both virtual machines.  
**Network Setup**  
Both Kali Linux and Metasploitable 2 were configured to use the  
   
 **Internal Network** option in VirtualBox.  
- **Kali Linux:** Connected to the isolated internal network.  
- **Metasploitable 2:** Connected to the same isolated internal  
   
 network.  
- **Network Name:** pmat-internalnetwork  
**Configuration Process**  
1. Opened **Oracle VirtualBox**.  
2. Selected the Kali Linux VM and opened **Settings → Network**.  
3. Under **Adapter 1**, enabled the network adapter.  
4. Changed **Attached to** from NAT to **Internal Network**.  
5. Created/selected the internal network named pmat-internalnetwork.  
6. Repeated the same configuration for the Metasploitable 2 VM,  
   
 ensuring both machines used the same internal network name.  
   
### **Why Use an Isolated Network?**  
- **Security:** Keeps the vulnerable target away from the normal network.  
- **Controlled Testing:** Allows Kali Linux to communicate with Metasploitable 2.  
- **Safe Environment:** Provides a dedicated environment for cybersecurity experiments.  
**Note:** VirtualBox Internal Network isolates these VMs from the host and external networks through that adapter. Both machines must use the same network name to communicate.  
### **Result**  
Successfully configured an isolated virtual network connecting Kali Linux and Metasploitable 2, creating a controlled environment for future penetration testing exercises.  
   
