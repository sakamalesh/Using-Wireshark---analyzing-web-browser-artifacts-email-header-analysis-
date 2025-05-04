# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:
Wireshark Web and Email Traffic Filtering Steps

## OUTPUT:
Captured Web Activity and Email Header Information
A. Capturing Traffic in Wireshark

1.Open Wireshark and start capturing on the active interface (Wi- Fi/Ethernet).

2.Perform activities like opening a website or sending an email through a client (e.g., Gmail via browser or Thunderbird).

3.Stop the capture once done.

![1](https://github.com/user-attachments/assets/6a17ac7f-0165-4cdb-87c8-950913072182)
### Analyze DNS Queries: o Filter: dns

o Reveal domains the browser tried to resolve.
![2](https://github.com/user-attachments/assets/fc502cc0-971c-4f3d-b58e-3b70360d5ffe)
Email Header Analysis

Apply relevant filters:
o For POP3: tcp.port == 110

o For SMTP: tcp.port == 25 or 587

o For IMAP: tcp.port == 143 or 993

4.Locate email data:
o Look for SMTP packets to see sender/receiver email addresses.

o Use "Follow TCP Stream" to view the full email headers and body if unencrypted.

5.Extract Email Header Fields:

o Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.

![3](https://github.com/user-attachments/assets/92d4f9d2-1287-496a-bf91-b64f74d4856c)
![4](https://github.com/user-attachments/assets/e229dca6-3e67-4cde-896b-de76f6eb2c97)
![5](https://github.com/user-attachments/assets/9f77307c-44fb-4507-9959-a7f315aa17b9)

## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark.

