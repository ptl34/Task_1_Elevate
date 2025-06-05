# Task_1_Elevate

# Step 1: Install Nmap
# Install nmap from official  website, configure and  verify nmap latest version 
 sudo apt install nmap

# Step 2: Find Your Local IP Range
ifconfig OR ip a

# Step 3 Run TCP SYN Scan with Nmap
nmap -sS subnet(ip range) -oN network_scan.txt 
# network_scan.txt store output in txt formate

# Step 4: Note Down IPs and Open Ports
Nmap will output a list of IPs in the subnet with open ports and services.

#  Step 5: Analyze Packets with Wireshark
Download and install Wireshark from official site

Start capturing on your active network interface.

Run your Nmap scan while Wireshark is capturing to see detailed packet info.

Stop capture after scan completes.

Use Wireshark filters like tcp or ip.addr == 192.168.1.10 to analyze.

# Step 6: Research Services
Look up common ports and their default services:

22 → SSH

80 → HTTP (web server)

443 → HTTPS

21 → FTP

3389 → RDP

Google: port 22 service, etc

# Step 7: Identify Security Risks
Open ports could mean potential attack surfaces.

Some services may be vulnerable or misconfigured.

Research CVEs or known exploits for those services.

# Step 8: Save Scan Results
Save your scan output to a file (text or HTML):

For text output:

nmap -sS ip_range(subnet) -oN scan_results.txt

For XML output (can convert to HTML later):
nmap -sS ip_range(subnet) -oX scan_results.xml



