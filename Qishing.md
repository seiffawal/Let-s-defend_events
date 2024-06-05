```md
EventID :
214
Event Time :
`Jan, 01, 2024, 12:37 PM`
Rule :
# SOC251 - Quishing Detected (QR Code Phishing)
Level :
Security Analyst
`SMTP Address :158.69.201.47`


# Source Address :
security@microsecmfa.com 

# Destination Address :
Claire@letsdefend.io
# E-mail Subject :
New Year's Mandatory Security Update: Implementing Multi-Factor Authentication (MFA)
Device Action :
- Allowed
- Incident Name:	EventID: 214 - [SOC251 - Quishing Detected (QR Code Phishing)]
- Description:	EventID: 214
- Incident Type:	Exchange
- Created Date:	May, 18, 2024, 01:15 PM

```
mail content

![image](https://github.com/seiffawal/Let-s-defend_events/assets/83987697/90af576c-0765-4bbc-85da-0957ba7a47e1)

```txt

Hello Claire,

You are mandated to update and enable 2FA security on your account as of 02/01/2024 to mitigate theft and help protect your account. Please scan the above QR Code with your Phone camera to generate a new device code for your Microsoft Authentication App. Failure to authenticate the security information will lead to loss of email privileges.

QR Code
Alternatively, you can use your phone's camera or visit websites equipped to scan QR codes.

Please be aware that failure to comply with this security update within the specified timeframe may lead to your account being blocked.

Happy New Year,
The Microsoft team

```
`link payload: https://ipfs.io/ipfs/Qmbr8wmr41C35c3K2GfiP2F8YGzLhYpKpb4K66KU6mLmL4#`
```txt
Alarms escalated from Tier1 to Tier2 should be caused by a truly harmful event, but escalated alarms by Tier1 analysts are not always True Positive due to technical inadequacy, faulty/incomplete analysis, and authorization problems. Before initiating Incident Response processes, please verify that the alarm from the Tier1 analyst was caused by malicious activity.
```
```yaml
Field
type

source_address
158.69.201.47

source_port
451
destination_address
172.16.20.3

destination_port
25

time
Jan, 01, 2024, 12:00 PM

Value
Raw Log

Exchange

Sender Mail

security@microsecmfa.com

Destination Mail

Claire@letsdefend.io

Subject

New Year's Mandatory Security Update: Implementing Multi-Factor Authentication (MFA)

Device Action

Allowed
```
## process log
```yml

No Process ID
Chrome.exe
—
c:/program files (x86)/google/chrome/application/chrome.exe

No Process ID
hh.exe
—
C:/Windows/hh.exe

No Process ID
ccsvchst.exe
—
c:/program files (x86)/symantec/symantec endpoint protection/14/bin/ccsvchst.exe

No Process ID
notepad.exe
—
c:/windows/system32/notepad.exe

No Process ID
powershell.exe
—
No Command

No Process ID
AcroRd32.exe
—
c:/program files (x86)/adobe/acro
```
## cmd log
```yaml
2020-10-10 10:29:01
cls
2020-10-10 10:29:02
net user
2020-10-10 10:29:03
net user backupUser
2020-10-10 10:29:04
net localgroup backupGroup backupUser /add
```
```vendors report https://www.virustotal.com/gui/ip-address/158.69.201.47 ```
