# BlueMoon-2021 System Hacking

**Student:** Nur Awadah  
**Target Machine:** BlueMoon-2021  
**Platform:** VulnHub  
**Attacker Machine:** Kali Linux  
**Virtualization:** Oracle VirtualBox

## Lab Environment

| Component | Description |
|---|---|
| Attacker | Kali Linux |
| Target | BlueMoon-2021 |
| Platform | VirtualBox |
| Network | Host-only Adapter |

## 1. Network Configuration

### Figure 1: Host-Only Network Configuration

Both Kali Linux and BlueMoon-2021 virtual machines were configured to use the same Host-Only Adapter in Oracle VirtualBox. This allows both machines to communicate within the isolated lab network.

<p align="center">
  <img src="screenshots/01-virtualbox-setup.png" width="400">
  <img src="screenshots/02-virtualbox-setup.png" width="400">
</p>
Both Kali Linux and BlueMoon-2021 virtual machines were started successfully. The Kali Linux IP address was checked using the `ip -br a` command.
<img src="screenshots/03.png" width="500">

The connectivity between Kali Linux and the BlueMoon-2021 target machine was tested using the ping command. 
The target responded successfully, confirming that both machines could communicate with each other.
<img src="screenshots/04.png" width="500">
