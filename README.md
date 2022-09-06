# I2P Java Software Guide
I2P Java Software Guide

# The I2P Router Console

This is where you can see your network connections and information about your router. You will be able to see how many peers you have, and other information that will help if you need to troubleshoot. You can stop and start the router as well. You will see the applications that the software includes, as well as links to some community forums and sites on the I2P network. You will receive news when there is a a new software release, and will be able to download the latest version here as well. Additionally, you can find shortcuts to other available applications. The console is customizable and includes a default light theme with a dark theme option.

# Sidebar Error Messages and what they mean

OK: Your UDP port does not appear to be firewalled.

Firewalled: Your UDP port appears to be firewalled. As the firewall detection methods are not 100% reliable, this may occasionally be displayed in error. However, if it appears consistently, you should check whether both your external and internal firewalls are open for your port. 

I2P will work fine when firewalled, there is no reason for concern. When firewalled, the router uses "introducers" to relay inbound connections. However, you will get more participating traffic and help the network if you open your firewall. If you think you have already done so, remember that you may have both a hardware and a software firewall, or be behind an additional, institutional firewall you cannot control. Also, some routers cannot correctly forward both TCP and UDP on a single port, or may have other limitations or bugs that prevent them from passing traffic through to I2P.

Testing: The router is currently testing whether your UDP port is firewalled.

Hidden: The router is not configured to publish its address, therefore it does not expect incoming connections. Hidden mode is automatically enabled for added protection in certain countries. Too see the countries that are on this list refer to the Strict Countries List.
WARN - Firewalled and Fast: You have configured I2P to share more than 128KBps of bandwidth, but you are firewalled. While I2P will work fine in this configuration, if you really have over 128KBps of bandwidth to share, it will be much more helpful to the network if you open your firewall.

WARN - Firewalled and Floodfill: You have configured I2P to be a floodfill router, but you are firewalled. For best participation as a floodfill router, you should open your firewall.

WARN - Firewalled with Inbound TCP Enabled: You have configured inbound TCP, however your UDP port is firewalled, and therefore it is likely that your TCP port is firewalled as well. If your TCP port is firewalled with inbound TCP enabled, routers will not be able to contact you via TCP, which will hurt the network. Please open your firewall or disable inbound TCP above.

WARN - Firewalled with UDP Disabled: You have configured inbound TCP, however you have disabled UDP. You appear to be firewalled on TCP, therefore your router cannot accept inbound connections. Please open your firewall or enable UDP.

ERR - Clock Skew: Your system's clock is skewed, which will make it difficult to participate in the network. Correct your clock setting if this error persists.

ERR - Private TCP Address: You must never advertise an unroutable IP address such as 127.0.0.1 or 192.168.1.1 as your external address. Correct the address or disable inbound TCP on the Network Configuration page.

ERR - SymmetricNAT: I2P detected that you are firewalled by a Symmetric NAT. I2P does not work well behind this type of firewall. You will probably not be able to accept inbound connections, which will limit your participation in the network.

ERR - UDP Port In Use - Set i2np.udp.internalPort=xxxx in advanced config and restart: I2P was unable to bind to the configured port noted on the advanced network configuration page . Check to see if another program is using the configured port. If so, stop that program or configure I2P to use a different port. This may be a transient error, if the other program is no longer using the port. However, a restart is always required after this error.

ERR - UDP Disabled and Inbound TCP host/port not set: You have not configured inbound TCP with an address and port on the Network Configuration page, however you have disabled UDP. Therefore your router cannot accept inbound
connections. Please configure a TCP host and port on the Network Configuration page or enable UDP.

ERR - Client Manager I2CP Error - check logs: This is usually due to a port 7654 conflict. Check the logs to verify. Do you have another I2P instance running? Stop the conflicting program and restart I2P.

# SusiMail (Developed by: postman, susi23, mastiejaner)
![img](https://user-images.githubusercontent.com/50714166/188678059-289fe956-9c27-495a-bae2-7158ac010b84.png)

SusiMail is a secure email client. It is primarily intended for use with Postman’s email servers inside of the I2P network . It is designed to avoid leaking information about email use to other networks. SusiMail is bridged so it can send and receive email from the internet as well. Occasionally you may see some services like Gmail classifying it as spam, which you can correct in your Internet email service providers settings.

Postman’s service offers both internal and external email with POP3 and SMTP service through I2PTunnel. This allows people to use their preferred mail clients to send and receive mail pseudonymously.

Most mail clients expose substantial identifying information, however, SusiMail has been built specifically with I2P's anonymity abilities in mind. The I2Pmail/mail.i2p service offers transparent virus filtering as well as denial of service prevention with hashcash augmented quotas.
In addition, each user has control of their batching strategy prior to delivery through the mail.i2p outproxies, which are separate from the mail.i2p SMTP and POP3 servers. Both the outproxies and inproxies communicate with the mail.i2p SMTP and POP3 servers through I2P itself, so compromising those non-anonymous locations does not give access to the mail accounts or activity patterns of the user. More information can be found on the I2P Site: hq.postman.i2p.xyz.

SusiMail can be accesed from the router console. 
![img](https://user-images.githubusercontent.com/50714166/188678062-ca64d7fa-b511-4296-908f-94b7fbd28157.png)
