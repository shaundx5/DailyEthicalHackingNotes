##  What is a Computer Network?
A network is a set of connected devices that communicate to share data and services. Examples include:
- **LAN**: Inside a building.
- **WAN**: Across cities.
- **Internet**: The global network.

---

## Subnet – Why It Matters
A **subnet** splits a large network into manageable pieces.
- Helps isolate sections of a network.
- Devices within a subnet talk directly.
- Makes things more secure and efficient.

---

##  IP Address Explained
- A unique number assigned to every device on a network.
- **IPv4** → Shorter, older version: `192.168.0.1`
- **IPv6** → Longer, future-ready: `2001:db8::1`

---

## 🆔 What is a MAC Address?
Every device’s network hardware has a unique **MAC address**.
- Looks like: `AA:BB:CC:DD:EE:FF`
- It's permanent and burned into the hardware.

---

##  IPv4 vs IPv6

| Key Difference | IPv4                    | IPv6                              |
|----------------|-------------------------|-----------------------------------|
| Bit Size       | 32-bit                  | 128-bit                           |
| Looks Like     | 192.168.1.1             | 2001:db8:1234::abcd               |
| Space          | Limited (~4.3B)         | Massive (virtually infinite)      |
| Security       | Add-on (IPSec optional) | Built-in IPSec                    |

---

## TCP vs UDP Quickfire

| Aspect        | TCP                          | UDP                       |
|---------------|-------------------------------|----------------------------|
| Connection    | Established (3-way handshake) | No connection             |
| Reliability   | Guaranteed with ACKs          | No guarantee              |
| Speed         | Slower but reliable           | Faster, best effort       |
| Example Use   | File transfer, emails         | Gaming, video streaming   |

---

## Port Forwarding – What & Why?
Allows access to a device inside your network from outside.
- Example: You can reach your home PC remotely using a forwarded port like `3389`.

---

##  UAC (User Account Control)
Windows feature that stops apps from making changes without your permission.
- You’ve seen those popups asking for admin access? That’s UAC.

---

##  Info Gathering Styles

| Mode   | Action Type              | Tools/Methods                    |
|--------|--------------------------|----------------------------------|
| Passive| No contact with target   | Google, Shodan, WHOIS            |
| Active | Target is probed         | Nmap, ping, traceroute           |

---

##  Nmap – Why Hackers & Admins Use It
Nmap helps scan networks and devices. You can:
- Detect hosts
- See which ports are open
- Get OS info and service versions

---

##  Sample Attack Timeline

1. Phishing email contains `.zip` file.
2. User enters password & extracts `.exe`.
3. File runs, opens a connection to the attacker.
4. PowerShell scripts are delivered silently.
5. UAC pop-ups are spammed to trick user.
6. Once allowed, system is fully exposed.

 Tip: Never run executables you didn't expect. Even from someone you know.

---

##  Nmap Command in Pieces

Command:
```bash
nmap -Pn -A -sV -O -oN --script -vv -p -sS -sT
```

| Flag       | What It Does                                                   |
|------------|----------------------------------------------------------------|
| `-Pn`      | Skip pinging – treat all hosts as live                         |
| `-A`       | Enable OS detection, version info, and traceroute              |
| `-sV`      | Shows service versions                                         |
| `-O`       | Tries to identify the OS                                       |
| `-oN`      | Saves readable output                                          |
| `--script` | Runs built-in scripts                                          |
| `-vv`      | Extra verbosity                                                |
| `-p`       | Lets you choose ports                                          |
| `-sS`      | SYN scan (quiet TCP scan)                                      |
| `-sT`      | TCP connect scan (fallback if SYN fails)                       |
