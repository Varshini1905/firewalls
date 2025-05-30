# 🔒 Linux Firewall Configuration: Step-by-Step Guide

This guide will help you configure the Ubuntu firewall to block and test inbound Telnet traffic on port 23 using `ufw` (Uncomplicated Firewall).

---

## 1️⃣ Open Terminal

You can open the terminal by:

- Searching for **"Terminal"** in the application menu  
**OR**  
- Pressing **Ctrl + Alt + T**

---

## 2️⃣ Check Current Firewall Rules

To check the status and see the currently configured firewall rules:

```bash
sudo ufw status verbose
```
---

3️⃣ Block Inbound Traffic on Port 23 (Telnet)
To block TCP traffic on port 23 (commonly used for Telnet):

```bash
sudo ufw deny 23/tcp
```
-----

4️⃣ Install Telnet Client (If Not Already Installed)
If telnet is not installed on your system, install it with:

```bash
sudo apt update
sudo apt install telnet -y
```
---
5️⃣ Test the Rule by Attempting to Connect to Port 23
Try connecting to port 23 locally to verify the block:

```bash
telnet localhost 23
```
✅ You should receive a connection failed message, which confirms that the port is successfully blocked.
---

6️⃣ Allow SSH Access (Port 22)
To ensure that SSH remains accessible:

```bash
sudo ufw allow 22/tcp
```
🔐 This is important if you're accessing the system remotely via SSH.


![Screenshot 2025-05-30 203109](https://github.com/user-attachments/assets/c75fae01-a5c2-4e4d-9e0b-7ffaea0c168c)
---

7️⃣ Remove the Block Rule for Port 23
To remove the Telnet block rule from the firewall:

```bash
sudo ufw delete deny 23/tcp
```
![Screenshot 2025-05-30 203446](https://github.com/user-attachments/assets/f3cc4e38-3269-430b-a550-7c7056ec5a0a)
---


