# Simple Mail Transfer Protocol-Enumeration (SMTP-Enum)

## Description
 The Simple Mail Transfer Protocol (SMTP) is a protocol for sending emails in an IP network. It can be used between an email client and an outgoing mail server or between two SMTP servers. SMTP is often combined with the IMAP or POP3 protocols, which can fetch emails and send emails. In principle, it is a client-server-based protocol, although SMTP can be used between a client and a server and between two SMTP servers. In this case, a server effectively acts as a client.

## Scope
 Enumerate the SMTP service banner along with its version. Then further enumerate the smtp service to find the username that exits on the clients system.

## Approach
 When enumerating the SMTP service, I used the command ![image](https://github.com/user-attachments/assets/b4811e11-81b3-414c-a155-dc024b117b7c) to connect to the SMTP service on port 25 and retrieve its banner, including the version information.

 ### Example 
![image](https://github.com/user-attachments/assets/1444e32f-7ffa-445e-898c-6db66c9b172b)

 To further enumerate the SMTP service and potentially discover valid usernames on the system, I used techniques such as the ![image](https://github.com/user-attachments/assets/4c004366-75fa-443e-8475-e77197405c06)
 command. This command, if enabled on the SMTP server, allows user verification, while the ![image](https://github.com/user-attachments/assets/cae986f1-5e23-4db7-99f9-56f50f33e8a7) command can expand mailing lists if necessary. I then performed a full scan of the username list using the command ![image](https://github.com/user-attachments/assets/3ec1bd91-d717-40d5-b7f7-6e39632679b2), which verified (VRFY) users on the system.

 ### Example
![image](https://github.com/user-attachments/assets/45404145-bc5e-4c45-9b92-686843919094)

## Notes
- Many modern SMTP servers have some commands disabled for security reasons. If ![image](https://github.com/user-attachments/assets/4c004366-75fa-443e-8475-e77197405c06) and ![image](https://github.com/user-attachments/assets/cae986f1-5e23-4db7-99f9-56f50f33e8a7) are disabled, the approach I have taken above may not work, and alternative methods like brute-force enumeration or social engineering may be needed.
- Once I've ran these command(s), any valid username(s) was revealed in the responses.
