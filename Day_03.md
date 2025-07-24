## Introduction to Git & Cloning

- **Git**: A version control system that allows developers to track changes in their code and collaborate with others.
- **git clone**: This command is used to **copy (clone) a repository from a remote server like GitHub** onto your local machine.

    ```bash
    git clone <repository-URL>
    ```

  This creates a local copy of the repository, so you can work on it offline.

---

## Two Types of Malware Analysis

### 1. Static Analysis

- Analyzing a file **without running it**.
- Involves checking properties such as:
    - File type (e.g., `.exe`, `.apk`)
    - Metadata
    - Strings inside the file
    - Code structure (using disassemblers)
- Considered safe since the malware is not executed.

### 2. Dynamic (Runtime) Analysis

- Involves **running the file in a controlled environment** to observe how it behaves in real time.
- Can reveal:
    - Files it creates or modifies
    - Network connections it attempts
    - Changes in system performance

---

## Sandbox

- A **sandbox** is a **virtual, isolated environment** for safely running suspicious files without risking your main system.
- Sandboxes are commonly used in dynamic analysis.
- Files such as `.exe` and `.apk` are often analyzed this way.

---

## ATS Software

- ATS stands for **Advanced Threat Simulation** (or similar).
- Specialized tools designed to:
    - Detect sophisticated threats
    - Simulate attack scenarios
    - Analyze malware behavior
- Typically part of professional cybersecurity toolkits.

---

## Linux Commands for Cybersecurity

### Basic File & Directory Operations

- `ls`: List contents of the current directory.
- `cd`: Change the current directory.
- `pwd`: Print your **current directory** path.
- `mkdir`: Create a **new directory**.
- `rmdir`: **Remove a directory** (must be empty).
- `cp`: **Copy files or directories**.
- `mv`: **Move or rename files or directories**.
- `man`: Open the **manual page** for a command.
- `echo`: Print a message to the terminal.
- `chmod`: Change file permissions (read, write, execute).
- `clear`: Clear your terminal screen.

> **Note:** Linux is **case-sensitive**.

---

### File Creation Methods

- Create an empty file using:
    ```bash
    touch hacker.txt
    ```
- To view file details:
    ```bash
    ls -lh
    ```
    - `l`: long listing (permissions, owner, date, etc.)
    - `h`: human-readable sizes (KB, MB)

---

### File Permissions Basics

In Linux, each file has permissions for:
- **Owner** (creator of the file)
- **Group** (other users in the same group)
- **Others** (everyone else)

To modify permissions, use:
```bash
chmod [permissions] [filename]
