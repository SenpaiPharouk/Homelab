# Lab Setup

| Machine | Role | IP |
|---|---|---|
| Kali Linux | Attacker | 192.168.100.10/24 |
| Metasploitable 2 | Target | 192.168.100.20/24 |

## Network
- Hypervisor: VirtualBox
- Both VMs use Adapter 1 on an **Internal Network** named `pmat-internalnetwork`
- No DHCP server, so both IPs are static
- No route to my home network or the internet during all scans

## Kali (permanent address with NetworkManager)
    sudo nmcli connection modify "Wired connection 1" ipv4.method manual ipv4.addresses 192.168.100.10/24
    sudo nmcli connection up "Wired connection 1"

## Metasploitable (permanent address)
Edited /etc/network/interfaces:

    auto eth0
    iface eth0 inet static
    address 192.168.100.20
    netmask 255.255.255.0

## Verification
    ping -c 3 192.168.100.20
    nmap -sn 192.168.100.0/24   # 2 hosts up

## Note
After the scans were done, a temporary NAT adapter was added to Kali only to push files to GitHub. Metasploitable stayed isolated, and no scans ran while NAT was on.
