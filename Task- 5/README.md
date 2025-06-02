# Elevate-Labs-Internship-Task 5

# Live Packet Capture and Protocol Identification

## 🎯 Objective
Capture live network packets using Wireshark and identify at least three protocols from the captured traffic.

---

## 🛠 Tools Used
- **Wireshark** (installed via `sudo apt install wireshark`)
- **Kali Linux Terminal** (used to ping and generate traffic)
- **Firefox browser** (used to create HTTP/DNS traffic)

---

## 🔁 Steps Performed

### 1. Started Wireshark:
```bash
wireshark


2. Captured on active interface: eth0
3. Generated traffic by:
And visiting https://example.com in the browser.

4. Stopped the capture after ~1 minute.
ping google.com

```

| Protocol | Wireshark Filter | Description                     |
| -------- | ---------------- | ------------------------------- |
| DNS      | `dns`            | Show only DNS queries/responses |
| HTTP     | `http`           | Show HTTP requests/responses    |
| ICMP     | `icmp`           | Show ping requests/replies      |
| TCP      | `tcp`            | Show all TCP packets            |
| UDP      | `udp`            | Show all UDP packets            |



 Task 5 – Wireshark Packet Capture

## 🔍 Objective
Capture live traffic and identify different network protocols using Wireshark.

## ✅ Protocols Identified

### 1. DNS
- Port: 53
- Usage: Domain name resolution
- Example Packet: `Standard query A for google.com`

### 2. HTTP
- Port: 80
- Usage: Website request (non-encrypted)
- Example Packet: `GET / HTTP/1.1`

### 3. ICMP
- Usage: Ping command (Echo request and reply)
- Example Packet: `Echo (ping) request to 142.250.183.110 (google.com)`

## 🔧 Tools Used
- Wireshark (Kali Linux)
- Browser and ping command

## 📌 Summary
Using Wireshark, I captured live network traffic and successfully identified common protocols like DNS, HTTP, and ICMP. Display filters helped isolate specific packet types and understand their structure and purpose.
