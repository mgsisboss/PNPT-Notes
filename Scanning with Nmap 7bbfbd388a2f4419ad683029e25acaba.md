# Scanning with Nmap

[https://www.notion.so](https://www.notion.so)

- Find Target  (both VMs are on Kali and Kioptrix on Nat Network
    - sudo arp-scan -l
    
    ![Untitled](Scanning%20with%20Nmap%207bbfbd388a2f4419ad683029e25acaba/Untitled.png)
    
    - sudo netdiscover -r 192.168.20.0/24
        
        ![Untitled](Scanning%20with%20Nmap%207bbfbd388a2f4419ad683029e25acaba/Untitled%201.png)
        
- Target 192.168.20.5   Now we use Nmap
    - nmap -T4 -p- -A 192.168.20.5 -oN /home/mgsisboss/PNPT/PEH/Kioptrix/Nmap.txt
        - T4: Stands for time T4 being the fastest
        - -p- scans all ports we can specify specific port ex.  -p 445
        - -A stands for everything fingerprinting, version, OS detection etc.
        - -oN     1. Syntax: nmap -oN </path/filename.txt> <target>
    
    ![Untitled](Scanning%20with%20Nmap%207bbfbd388a2f4419ad683029e25acaba/Untitled%202.png)
    
- nmap -T4 -sU --top-ports 1000 192.168.20.5 -oN /home/mgsisboss/PNPT/PEH/Kioptrix/Nmap_UPD.txt
    - UDP scans take longer, so specify the top 1000 common ports.
    - UDP is connectionless, so it does not have to acknowledge.
        - 
        
        ![Untitled](Scanning%20with%20Nmap%207bbfbd388a2f4419ad683029e25acaba/Untitled%203.png)
        
    

[Enumerating HTTP/HTTPS](Scanning%20with%20Nmap%207bbfbd388a2f4419ad683029e25acaba/Enumerating%20HTTP%20HTTPS%2062f5fe6eadb14389bca5efd487c7181c.md)