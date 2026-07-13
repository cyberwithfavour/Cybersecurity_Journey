DAY 8 — Linux Networking Fundamentals

🧠 Notes

Today I learned the basics of Linux networking and how devices communicate over a network.

Key Concepts:

* Every device on a network has an IP address
* Network interfaces connect a system to a network
* Linux uses interfaces such as lo and enp0s3
* DNS translates domain names into IP addresses
* Connectivity issues can occur because of network or DNS problems
* Network troubleshooting is an important cybersecurity skill

Commands:

* ip a → Display IP address information
* ip link → Show network interfaces
* hostname → Display system hostname
* ping google.com → Test connectivity and DNS resolution
* ping 8.8.8.8 → Test connectivity using an IP address
* nslookup google.com → Query DNS information

Observations:

* My Ubuntu VM received the IP address 10.0.2.15
* The active interface was enp0s3
* DNS resolution failed with a SERVFAIL error
* Direct connectivity to 8.8.8.8 also failed
* These results indicate a network configuration issue inside the virtual machine

Cybersecurity Relevance:

Network analysts and SOC analysts use networking tools to investigate connectivity issues, suspicious traffic, and communication between systems.
  
