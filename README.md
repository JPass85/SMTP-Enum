# Simple Mail Transfer Protocol-Enumeration (SMTP-Enum)

## Description
 The Simple Mail Transfer Protocol (SMTP) is a protocol for sending emails in an IP network. It can be used between an email client and an outgoing mail server or between two SMTP servers. SMTP is often combined with the IMAP or POP3 protocols, which can fetch emails and send emails. In principle, it is a client-server-based protocol, although SMTP can be used between a client and a server and between two SMTP servers. In this case, a server effectively acts as a client.

## Scope
 Enumerate the SMTP service banner along with its version. Then further enumerate the smtp service to find the username that exits on the clients system.

## Approach
 When enumerating the smtp service banner, I used the following (telnet <10.xxx.xxx.xxx> 25> command to connect to the SMTP service on port 25 retrieve its banner along with version.

 ### Example

![image](https://github.com/user-attachments/assets/1444e32f-7ffa-445e-898c-6db66c9b172b)


