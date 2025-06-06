# 🚀 Task 4 – Firewall Configuration and Testing (UFW)

## 🎯 Objective
Configure and test basic firewall rules using UFW on Kali Linux to understand how firewalls filter network traffic.

Summary: How Firewalls Filter Traffic
A firewall filters traffic by inspecting incoming and outgoing packets and applying rules based on port, protocol, or IP. 

In this task, we:
Blocked an insecure service (Telnet on port 23)
Allowed secure remote access (SSH on port 22)
Verified and reversed the changes safely
UFW simplifies this process with easy-to-use commands compared to traditional iptables.

Outcome
Gained hands-on experience with:

Managing firewall rules

Testing rule behavior

Understanding basic network filtering logic


---

## 🛠 Tools Used
- **Operating System**: Kali Linux
- **Firewall**: UFW (Uncomplicated Firewall)

---

## 🔧 Commands Used

### 1. Install and Enable UFW
```bash
sudo apt update
sudo apt install ufw -y
sudo ufw enable

### 2. Check Current Rules
sudo ufw status numbered

### 3. Block Inbound Traffic on Port 23 (Telnet)
sudo ufw deny 23

### 4. Test the Rule
telnet localhost 23

### 5. Allow SSH (Port 22)
sudo ufw allow 22

### 6. Remove the Test Rule
sudo ufw status numbered
sudo ufw delete 1
