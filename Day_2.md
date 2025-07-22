## Day 02: Tools and Setup

### GitHub Workflow

- *Account Creation:* [https://github.com/](https://github.com/)
- *Fork Existing Repo:* Click *Fork* to copy others’ repositories.
- *Create New Repository:*
  1. Click *New Repository*.
  2. Fill repository details.
  3. Choose visibility (Public/Private).
  4. Click *Create Repository*.

---

### VirtualBox & Kali Linux

- *VirtualBox:* Virtualization platform for creating VMs.
- *Kali Linux:* Debian-based OS used for cybersecurity tasks.

#### Installation Process:
1. Install VirtualBox.
2. Download Kali Linux (ISO or OVA).
3. In VirtualBox:
   - *Option A:* Import OVA.
   - *Option B:* Create new VM, attach ISO/VDI.
   - Allocate *minimum 2 GB RAM*.
   - Set processors (recommended 2).
   - Start VM.

---

### 7zip Utility

Use *7zip* to extract compressed files.

Example:

7z x kali-linux-2025.2-virtualbox-amd64.7z


---

### Error Handling

| Problem                  | Solution                                     |
|--------------------------|----------------------------------------------|
| Hyper-V conflict         | Disable Hyper-V in Windows Features.         |
| Missing bootable media   | Ensure ISO/OVA is attached before boot.      |
| RAM allocation failure   | Set at least 2 GB RAM.                       |
| VT-x/AMD-V errors        | Enable virtualization in BIOS settings.      |

---
