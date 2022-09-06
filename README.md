# I2P Java Software Guide
I2P Java Software Guide

# SusiMail (Developed by: postman, susi23, mastiejaner)
![img](https://user-images.githubusercontent.com/50714166/188678059-289fe956-9c27-495a-bae2-7158ac010b84.png)

SusiMail is a secure email client. It is primarily intended for use with Postman’s email servers inside of the I2P network . It is designed to avoid leaking information about email use to other networks. SusiMail is bridged so it can send and receive email from the internet as well. Occasionally you may see some services like Gmail classifying it as spam, which you can correct in your Internet email service providers settings.

Postman’s service offers both internal and external email with POP3 and SMTP service through I2PTunnel. This allows people to use their preferred mail clients to send and receive mail pseudonymously.

Most mail clients expose substantial identifying information, however, SusiMail has been built specifically with I2P's anonymity abilities in mind. The I2Pmail/mail.i2p service offers transparent virus filtering as well as denial of service prevention with hashcash augmented quotas.
In addition, each user has control of their batching strategy prior to delivery through the mail.i2p outproxies, which are separate from the mail.i2p SMTP and POP3 servers. Both the outproxies and inproxies communicate with the mail.i2p SMTP and POP3 servers through I2P itself, so compromising those non-anonymous locations does not give access to the mail accounts or activity patterns of the user. More information can be found on the I2P Site: hq.postman.i2p.xyz.

SusiMail can be accesed from the router console. 
![img] (
