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


<img width="1083" height="763" alt="Screenshot 2026-09-01 141653" src="https://github.com/user-attachments/assets/b1e38646-8626-4873-928e-569c2cf40645" />



PROTOCOLS OBSERVED


1. ARP

   
Wireshark filter: arp


Reason for the search:

The ARP filter was used to identify Address Resolution Protocol traffic and observe how a device discovers the MAC address associated with an IPv4 address on the local network.


An example observed packet was:
Who has 192.168.10.2?

<img width="1066" height="740" alt="Screenshot 2026-09-01 142943" src="https://github.com/user-attachments/assets/aa982f34-f9e3-455e-a76f-9913b71ffa30" />





2. ICMP

   
Wireshark filter: icmp


Reason for the search:

The ICMP filter was used to identify packets generated during a ping test. ICMP Echo Request and Echo Reply packets are commonly used to test network connectivity.

<img width="1077" height="747" alt="Screenshot 2026-09-01 143058" src="https://github.com/user-attachments/assets/3249e4b3-ba08-40dd-b2d3-34f69dfca303" />





3. DHCP

   
Wireshark filter: dhcp


Reason for the search:

The DHCP filter was used to examine how network configuration is automatically provided to a device.


An observed DHCP packet had:

Source port: UDP 68

Destination port: UDP 67

UDP port 68 is used by the DHCP client, while UDP port 67 is used by the DHCP server.

<img width="1015" height="730" alt="Screenshot 2026-09-01 143239" src="https://github.com/user-attachments/assets/0473935a-a722-4e2d-96aa-d7b3d4235bd8" />

<img width="1138" height="377" alt="Screenshot 2026-09-01 143540" src="https://github.com/user-attachments/assets/755295ca-a2b3-4233-a8cf-d0a55fe2dbf1" />






4. DNS

   
Wireshark filter: dns


Reason for the search:

The DNS filter was used to examine how domain names are resolved into IP addresses.


An observed DNS packet had:

Source port: UDP 52974

Destination port: UDP 53

Port 52974 was an ephemeral client port, while UDP port 53 is the standard DNS service port.

<img width="1017" height="701" alt="Screenshot 2026-09-01 143828" src="https://github.com/user-attachments/assets/259d9827-f8c3-4cbd-9c5c-7aee11c51528" />

<img width="1147" height="483" alt="Screenshot 2026-09-01 143901" src="https://github.com/user-attachments/assets/0bc900cf-5208-4102-ad67-bb865ea7ae4b" />





5. UDP

   
Wireshark filter: udp


Reason for the search:

The UDP filter was used to identify User Datagram Protocol traffic. DHCP and DNS traffic observed during the practical used UDP.
Port Analysis

Common TCP ports such as 80 (HTTP) and 443 (HTTPS) were not observed in the captured traffic during this practical and therefore were not recorded as observed ports.

<img width="1009" height="768" alt="Screenshot 2026-09-01 144731" src="https://github.com/user-attachments/assets/c1356a5d-caf1-487e-b805-137e7f115c86" />

<img width="955" height="593" alt="Screenshot 2026-09-01 144810" src="https://github.com/user-attachments/assets/e55b1fe1-17fd-46b3-9fa3-b74940d6d509" />





Observations

The Wireshark capture showed several types of network traffic generated during normal network communication. ARP traffic was observed when the computer needed to identify a device on the local network. ICMP traffic was observed during the connectivity test, while DHCP traffic showed communication between the client and DHCP server. DNS traffic was observed when a domain name was accessed.
The practical demonstrated that network traffic contains useful information about protocols, IP addresses, ports, and communication between network devices.


Conclusion


The practical provided an understanding of how Wireshark can be used to monitor and analyze network traffic. By applying display filters, different protocols could be isolated and examined individually. The exercise also demonstrated the roles of ARP, ICMP, DHCP, DNS, and UDP in everyday network communication.
Wireshark is therefore a useful tool for network troubleshooting, monitoring, and cybersecurity analysis because it provides detailed information about packets travelling across a network.


<img width="1113" height="703" alt="Screenshot 2026-09-01 144840" src="https://github.com/user-attachments/assets/c563428f-66ef-4963-ac7f-dc23e21e8d72" />


