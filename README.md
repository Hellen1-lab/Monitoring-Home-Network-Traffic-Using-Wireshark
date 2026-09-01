# Monitoring-Home-Network-Traffic-Using-Wireshark

Introduction


Wireshark is a network protocol analyzer used to capture and examine network traffic. It allows users to observe different protocols and understand how devices communicate across a network.


This practical involved monitoring network traffic using Wireshark on Kali Linux running in VMware. The objective was to capture network packets, apply display filters, identify protocols, examine network communication, and analyze the ports used by different services.


Network Configuration


Operating System: Kali Linux


Virtualization Platform: VMware


Network Mode: NAT


Network Interface: eth0


DHCP: Enabled


Protocols Observed


1. ARP

   
Wireshark filter: arp


Reason for the search:

The ARP filter was used to identify Address Resolution Protocol traffic and observe how a device discovers the MAC address associated with an IPv4 address on the local network.


An example observed packet was:
Who has 192.168.10.2?


2. ICMP

   
Wireshark filter: icmp


Reason for the search:

The ICMP filter was used to identify packets generated during a ping test. ICMP Echo Request and Echo Reply packets are commonly used to test network connectivity.


3. DHCP

   
Wireshark filter: dhcp


Reason for the search:

The DHCP filter was used to examine how network configuration is automatically provided to a device.


An observed DHCP packet had:

Source port: UDP 68

Destination port: UDP 67

UDP port 68 is used by the DHCP client, while UDP port 67 is used by the DHCP server.


4. DNS

   
Wireshark filter: dns


Reason for the search:

The DNS filter was used to examine how domain names are resolved into IP addresses.


An observed DNS packet had:

Source port: UDP 52974

Destination port: UDP 53

Port 52974 was an ephemeral client port, while UDP port 53 is the standard DNS service port.


5. UDP

   
Wireshark filter: udp


Reason for the search:

The UDP filter was used to identify User Datagram Protocol traffic. DHCP and DNS traffic observed during the practical used UDP.
Port Analysis

Common TCP ports such as 80 (HTTP) and 443 (HTTPS) were not observed in the captured traffic during this practical and therefore were not recorded as observed ports.
Observations
The Wireshark capture showed several types of network traffic generated during normal network communication. ARP traffic was observed when the computer needed to identify a device on the local network. ICMP traffic was observed during the connectivity test, while DHCP traffic showed communication between the client and DHCP server. DNS traffic was observed when a domain name was accessed.
The practical demonstrated that network traffic contains useful information about protocols, IP addresses, ports, and communication between network devices.
Conclusion
The practical provided an understanding of how Wireshark can be used to monitor and analyze network traffic. By applying display filters, different protocols could be isolated and examined individually. The exercise also demonstrated the roles of ARP, ICMP, DHCP, DNS, and UDP in everyday network communication.
Wireshark is therefore a useful tool for network troubleshooting, monitoring, and cybersecurity analysis because it provides detailed information about packets travelling across a network.
