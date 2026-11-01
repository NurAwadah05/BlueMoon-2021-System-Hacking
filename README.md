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

Nmap was used to scan the target machine to identify open ports and running services.
The scan discovered FTP (21), SSH (22), and HTTP (80).
<img src="screenshots/05.png" width="500">

Gobuster was used to discover hidden directories on the target web server.
The /hidden_text directory was discovered during enumeration.
<img src="screenshots/06.png" width="500">

A hidden QR code image was downloaded from the target web server.
The QR code revealed FTP login information.The discovered credentials were:

- Username: `userftp`
- Password: `ftpp@ssword`

The script also contained an FTP command to connect to the target machine.
<img src="screenshots/07.png" width="500">
