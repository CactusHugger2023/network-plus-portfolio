
# Network Ports and Protocols

## Purpose
Ports and protocols are important because protocols define the rules for how devices exchange data, while ports direct that traffic to the exact application or service on a device. Protocols enable cross-device communication by providing different systems a shared set of rules to communicate by. They control the preference of Reliability (TCP) vs Speed (UDP) and they define service bahvior by specifying how those tasks work. ie web browsing (HTTP - 80/HTTPS - 443)

## Protocol Reference
| Protocol | Port | Transport | Purpose |
|---|---|---|---|
|FTP|20/21|TCP|Allows computers to upload and download files from another computer over a netowrk. Port 20 is for data transfer and port 21 for connection control and commands.|

|SSH|22|TCP|Facilitates remote access and control of another computer though a cmd line interface. SSH gives you a secure terminal on a remote machine, encrypting communication. SSH gives you a secure terminal on a remote machine, encrypting communication, supports password and key-based authentication, and provides the foundation for SFTP|

|SFTP|22|TCP|SFTP transfers files securely between computers ussing SSH. SFTP encrypts the file transfer and authentication process.|

|TELNET|23|TCP|Provides remote command-line access, like SSH however, it does not encrypt its communication and conducts it in plaintext.|

***SSH and Telnet both provide remote terminal access. FTP and SFTP both transfer files. SSH and SFTP share port 22 because SFTP operates through SSH.***

|---|---|---|---|
|---|---|---|---|
|---|---|---|---|
|---|---|---|---|
|---|---|---|---|
|---|---|---|---|
|---|---|---|---|
|---|---|---|---|
|---|---|---|---|
|---|---|---|---|
| HTTP | 80 | TCP | |
| HTTPS | 443 | TCP | |
| SSH | 22 | TCP | |
| DNS | 53 | TCP/UDP | |
| DHCP | 67/68 | UDP | |
| NTP | 123 | UDP | |

## Diagnostic Commands
Document nslookup, tracert, and
Test-NetConnection with examples.

## Common Confusions
Explain DNS vs DHCP and TCP vs UDP.

## Self-Test
Write 15 questions and their explanations.

## References
List learning resources.
