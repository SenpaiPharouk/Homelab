# Lessons Learned

## Technical
- **Default scans miss ports.** The top-1000 scan found 23 open ports, the full scan found 30. The 7 extras were 3632, 6697, 8787, 36147, 42081, 50048, 54997.
- **Versions matter more than port numbers.** "ftp" on port 21 is just a name. "vsftpd 2.3.4" is a known backdoor.
- **Scripts need verification.** Three NSE scripts failed, so their results prove nothing.
- **Network setup takes time.** Internal networks have no DHCP. Manual IPs and routes disappeared until I made them permanent with NetworkManager.

## My mistakes (all real)
| Mistake | Fix |
|---|---|
| `-sv` instead of `-sV` | Nmap options are case-sensitive |
| `-0` (zero) instead of `-O` | Letter O, not the number |
| `systemtl` instead of `systemctl` | Use Tab to autocomplete |
| `dhclient` not found | Newer Kali uses NetworkManager (`nmcli`) |
| Two commands on one line | One command per line |
| Running scans from `~` | `cd ~/nmap-project` first |
| Typo in `-oA scans/03-` | Check the filename before pressing Enter |
| Typed the wrong IP (`192.169`) | Read the target before running |

## What I would do next
- Run a UDP scan (`-sU --top-ports 50`)
- Compare against a hardened host
- Look at how a firewall or IDS would see these scans
