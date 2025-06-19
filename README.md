# My Home SOC Lab Project

## 🧠 Overview
This project documents the process of creating a home cybersecurity lab using VirtualBox, Kali Linux, and Windows 10.

## 🛠️ Tools Used
- VirtualBox
- Kali Linux
- Windows 10 VM
- Nmap
- Event Viewer (Windows)

## 🧪 Lab Setup Steps
1. Installed VirtualBox
2. Downloaded Kali Linux and Windows 10 VMs
4. Configure Host-only Networking
   1. Kali:
      ##### Make sure the VirtualBox adapter is enabled:
      + Kali VM > Settings > Network > Adapter 1
      + ✅ Ensure "Enable Network Adapter" is checked
      + Attached to: Internal Network
      + Cable Connected: ✅✔
      ##### Note: Repeat the above settings for Windows ( See image 1 )

      ##### Next, assign a Static IP ( See image 2 )
   3. Window:
      ##### Set Windows Network to Profile to Private ( See image 3 )

      ##### Enable ICMP (Ping) on Windows ( See image 4 )

      ##### Assign IP ( See image 5 )
      + Go to Control Panel > Network and Sharing Centre
      + Click Change adapter settings
      + Right-click your network adapter > Properties.
      + Select Internet Protocol Version 4 (TCP/IPv4), click Properties
      ##### Now, assign IP address, Subnet mask, Leave gateway and DNS blank, Click Ok
      
5. Tested Network Communication (**See Image 6**)
   ##### Kali Bash: Ip a or IfConfig
   ##### Ping (Window IP)
  
   ##### Window Command Prompt: Ipconfig (See Image 7)
   ##### Ping (Kali Linux IP)
  
7. Ran Nmap scan from Kali to Windows (**See Image 8**)
   + From Kali Bash run: nmap -sV (Windows IP)
   
9. Observed Windows event logs (See Log File)


## 🚀 Future Tasks
- Install Security Onion
- Simulate brute force attacks
- Create alert dashboards
