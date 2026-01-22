# Flashcards
## Lab 1
```flashy
In the lab topology, what is the IP address of the pfSense firewall's internal interface?
202.20.1.1 
172.30.0.2 
=172.30.0.1 
172.40.0.2 
---
What does the "-n" option in the tcpdump command "tcpdump -i eth0 -n host 202.20.1.1" do?
=Prevents conversion of addresses to names 
Specifies the network interface to listen on 
Limits the number of packets captured 
Filters packets by host IP address 
---
What does the command "ipconfig /all | findstr /i "ipv4 subnet mask physical"" do?
Displays all network adapter information 
Pings all devices on the network 
=Filters output to show only IPv4 address, subnet mask, and MAC address 
Clears the ARP cache 
---
What doesn't the ipconfig command display?
=Computer name 
Subnet mask 
IP address 
Default gateway 
---
What is the primary difference between a Regular scan and an Intense scan in Nmap/Zenmap?
An Intense scan works only on Linux systems. 
A Regular scan checks only for open ports. 
=An Intense scan uses more aggressive techniques to gather information. 
A Regular scan provides more detailed information than an Intense scan. 
---
What is the primary purpose of using the ARP command in network security analysis?
To map IP addresses to MAC addresses 
To display IP configuration 
To test network connectivity 
=To detect potential ARP spoofing attacks 
---
What is the purpose of sending a TCP SYN packet to a specific port using hping3?
=To test firewall rules or identify how the firewall handles traffic from different sources 
To establish a full TCP connection 
To perform a denial-of-service attack 
To clear the ARP cache 
---
What protocol does hping3 use when executing the command "hping3 -1 -c 1 202.20.1.1"?
UDP 
=ICMP 
ARP 
TCP 
---
Which command is used to display and configure network interface parameters in Linux?
ipconfig 
arp 
=ifconfig 
ping 
---
Which tool is described as a "comprehensive graphical packet analyzer" in the lab overview?
Hping3 
Nmap 
=Wireshark 
Tcpdump
```