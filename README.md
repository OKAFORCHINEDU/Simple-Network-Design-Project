# Simple_Network_Design_Project for CCNA Exam Preparation

#Project Description
This is a simple network design for a small company of less than 50 employees.

******Design requirements******

•	Each department should contain at least two PCs, one printer.
•	Appropriate number of switches and routers should be used in the network.
•	Using the given network 192.168.0,0/24 all interfaces shall be configured with correct IP addresses, subnet mask and gateways.
•	All devices in the network should be connected using appropriate cables.
•	Test communication between devices in both ACCOUNTS, Delivery and ENGINEERING departments.
•	Users can also connect wirelessly with the help of an Access Points
•	There should be one central web server, dns server
•	There should be a file server that only accounting department can have access to


******Business Requirements******

1.	The total number of staffs is <50 with foreseeable growth.
2.	Uninterrupted Internet service
3.	Email service
4.	Secure Network
5.	Low cost budget
6.	Office productivity suite

****Network devices required for this simplet network setup****

1. SOHO/SME WIRELESS ROUTER
2. 8 Port PoE managed access switch
3. Autonomous access points
4. File server
5. Category 5e UTP LAN cable
6. Two wireless printers
7. 30 personal computers

*****Suggested Vendor Devices*****

Switch

1. Cisco
- Cisco catalyst 2950 series refurbished.  
These are old cisco switches without support service from cisco. It now has PoE ports. They do not have the modern inbuilt tech such as advanced network monitoring, network automation and cloud. But they are affordable and can still get the job done.

- Cisco catalyst 2960 Series
 
2. Juniper

3. Mikrotik 

4. D-link 

5. Netgear


Router

Any 4 * 1G port SME/SOHO wirelessRouter

Access points

801.11ac capability access points.


********Configurations*******

Task
1- configured console login
password: egoamaka

2- configured line vty 0 -15 used for remote login, meaning 16 people can login at the same time via ssh/telnet
3- configured an ip on the vlan1 (192.168.0.253)  interface so the switch can be access remotely.
4- configured login so the switch will ask for a username during login
username: chinedu
password: egoamaka
5- configured ssh by first generating rsa keys with crypto, also, I created an ip domain (tyc.com) to be used by the rsa.
To be accessed on from management PC (192.168.0.10)

6. Server 1 (192.168.0.20) is configured as the syslog host.



****Employee Network Bandwidth Usage calculation****

This network is designed for 30 users.

User: Heavy
No: Employee: 10
Bandwidth: 100kbps
Total Bandwidth: 10 * 1000 = 10Mbps

User: Medium
No of employee: 15 
Bandwidth: 500kbps
Total Bandwidth: 15 * 500kbps = 7.5Mbps

User: Light
No of employees: 5 
Bandwidth: 200kbps
Total Bandwidth: 5 * 200kbps
= 1Mbps
Total Employee Bandwidth requirement = 10Mbps + 7.5Mbps + 1Mbps = 16.6Mbps
Required Bandwidth + Additional bandwidth for growth (3.5Mbps) = 20Mbps


Conversion of Bits to Byte to get the network speed.

Network Bandwidth / 8 
20Mbps/8 = 2.5MBps network speed.

Hence, the minimum network bandwidth required for efficient operating of this network setup is 20Mbps.

******Advanates of this SimpleNetwork Setup****

1. It is very easy to set up
2. low CapEx
3. few network devices
 4.It requires simple configuration
5.Users each department can easily connect to their accesspoint.
6. System activities of the switch is logged.
7. Network administrator not a must


****Disadvantages*****
1. It has one broadcast domain which leads to network inefficiency
2. Etherchannel cannot be configured on the home gateway wireless router becuase it doesn't have such feature. Hence, interface g0/1 will only movetoforwading state if g8/1 fails.

3. VoIP cannot be introduced.  Users can still use the internet to make calls and engage in video conferencing. But there should expected decrease in quality of service. 
4.VPN canot be introduced. This is because the features on the router is diabled.

5. Unilateral AP management: The three APs are autonomous and can be managed individually. This can introduce signal interference leading to decrease in network efficiency.
6. Not scalable and redundant. It has many Single point of failure


 
