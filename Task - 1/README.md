# Elevate Labs -Task- 1
This is result of nmap scan in which i scaned all ports, operating system, and servce version on my kali machine ip:

using this scan i identified that port 21/tcp was open in which ftp service was runing and version was vsftps 3.0.5


# Nmap 7.95 scan initiated Sun May 25 21:00:11 2025 as: /usr/lib/nmap/nmap -p- -sV -O -oN output1.txt 192.168.x.x
Nmap scan report for 192.168.x.x
Host is up (0.000066s latency).
Not shown: 65534 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 3.0.5
Device type: general purpose
Running: Linux 2.6.X|5.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:5 cpe:/o:linux:linux_kernel:6
OS details: Linux 2.6.32, Linux 5.0 - 6.2
Network Distance: 0 hops
Service Info: OS: Unix

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun May 25 21:00:14 2025 -- 1 IP address (1 host up) scanned in 3.32 seconds





This is result of nmap scan in which i scaned all ports with servce-version, operating system and TCP SYN Scan on my kali machine ip:



# Nmap 7.95 scan initiated Sun May 25 21:23:12 2025 as: /usr/lib/nmap/nmap -p- -sS -sV -O -oN output2.txt 192.168.x.x
Nmap scan report for 192.168.x.x
Host is up (0.000064s latency).
Not shown: 65534 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 3.0.5
Device type: general purpose
Running: Linux 2.6.X|5.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.32 cpe:/o:linux:linux_kernel:5 cpe:/o:linux:linux_kernel:6
OS details: Linux 2.6.32, Linux 5.0 - 6.2
Network Distance: 0 hops
Service Info: OS: Unix

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun May 25 21:23:15 2025 -- 1 IP address (1 host up) scanned in 3.15 seconds





Wireshark result in Below, in which i captured packets during second- nmap scap scan:





No.     Time           Source           Destination       Protocol Length Info
1       0.000000000    192.168.x.x      192.168.x.x       DNS      88     Standard query PTR x.x.x.x.in-addr.arpa

Frame 1: 88 bytes captured on interface eth0
Ethernet II, Src: xx:xx:xx:xx:xx:xx, Dst: xx:xx:xx:xx:xx:xx
IPv4, Src: 192.168.x.x, Dst: 192.168.x.x
UDP, Src Port: 33149, Dst Port: 53
DNS Query

2       0.032789168    MAC_A            Broadcast         ARP      60     Who has 192.168.x.x? Tell 192.168.x.x

3       0.032811339    MAC_B            MAC_A             ARP      42     192.168.x.x is at xx:xx:xx:xx:xx:xx

4       0.033016444    192.168.x.x      192.168.x.x       DNS      165    DNS response: No such name PTR x.x.x.x.in-addr.arpa

5       5.079463321    MAC_B            MAC_A             ARP      42     Who has 192.168.x.x? Tell 192.168.x.x

6       5.080186936    MAC_A            MAC_B             ARP      60     192.168.x.x is at xx:xx:xx:xx:xx:xx
