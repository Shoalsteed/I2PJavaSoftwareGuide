# I2P Java Software Guide
I2P Java Software Guide

# The I2P Router

The first time your I2P router makes connections to the network, it may take a few minutes to integrate your router into the network. As it begins to make this connection by finding peers, you will see the number of Active Peers begin to grow in the sidebar Peers status section.
When your router is ready, you will also see a Local Tunnel named Shared Clients listed there, and possibly other clients and servers. These Local Tunnels provide connections to the I2P network, enabling your bittorrent, email, web proxy and other services. Your Network Database indicates all known peers on the network. Additionally, you can monitor existing Peer Connections, and view existing Tunnels and their status. 

When the I2P router starts up, and during normal operation, the tunnel build readiness indicator in the sidebar may indicate that I2P is "Rejecting Tunnels." This is normal behaviour.

![img](https://user-images.githubusercontent.com/50714166/188688035-aed54954-d404-4d3e-a51e-942c22221b0f.png)


# The I2P Router Console

This is where you can see your network connections and information about your I2P router. You will be able to see how many peers you have, and other information that will help if you need to troubleshoot. You can stop and start the router as well. You will see the applications that the software includes, as well as links to some community forums and sites on the I2P network. You will receive news when there is a a new software release, and will be able to download the latest version here as well. Additionally, you can find shortcuts to other available applications. The console is customizable and includes a default light theme with a dark theme option.

**/home** 

![img](https://user-images.githubusercontent.com/50714166/138901134-6e1df8dc-cb93-4a7d-b6ef-fc6d4ec9081c.png)

This is the landing page of the I2P router console. It is comprised of a sidebar, news, and quick links to I2P applications, a selection of I2P sites, services, help and configuration.

*Sidebar*
The sidebar will display:
-what version of I2P you are running
-how long it has been running
-your router connection status
-tunnel build status
-alerts when a new version of I2P is available for download
-reseed if required
-options to stop, restart your router

*News*
The news section will display highlights from a new release, and alerts when there is a need to do an update to any plugins, or extensions or the I2P router software itself. This section can be displayed or hidden based on your preference.

*Applications*
The I2P router includes : I2P Addressbook , Email, Hidden Services Manager, Torrents, and a Web Server. This section provides links to each.

*I2P Community Sites*
This is a collection of sites and services that the I2P team hosts, with exception of the Tin Hat. They are are all internal to the I2P network.
They include links to zzz' dev forum, the community forum, the project Gitlab, and more. If you want to check if your browser is configured properly and if you are connected to the I2P network, click on one of these options to find out!

*Configuration and Help*
In this section you can access your bandwidth sharing options, help and FAQ , and add plugins to your router, or customize the look of your router console as part of the configuration options available.

*Network and Developer Information*
Links in this section include access to I2P technical docs, the project Bugtracker, Trac Wiki, and metrics options for people who are interested in I2P network statistics. Logs for your router can be accessed here as well.

**/console**

/console is a welcome page that provides information about error messages, warmings and troubleshooting information.

![img](https://user-images.githubusercontent.com/50714166/138901499-8df0e6a1-78cc-40c7-80e6-9a6aa91e1073.png)

# Sidebar Error Messages And What They Mean

*Reseed*: In some cases there are issues with finding Peers and connecting with the I2P network. If the router is encountering this issue, it will provide the option to "Reseed" in the sidebar. Clicking the Reseed button will fetch a bundle of Peers router infos

*OK*: Your UDP port does not appear to be firewalled.

![img](https://user-images.githubusercontent.com/50714166/188681416-502dd6e5-d2e5-4609-89df-d78af9c183e6.png)

*Firewalled*: I2P will work fine when firewalled, there is no reason for concern. When firewalled, the router uses "introducers" to relay inbound connections. However, you will get more participating traffic and help the network if you open your firewall. If you think you have already done so, remember that you may have both a hardware and a software firewall, or be behind an additional, institutional firewall you cannot control. Also, some routers cannot correctly forward both TCP and UDP on a single port, or may have other limitations or bugs that prevent them from passing traffic through to I2P.

*Testing*: The router is currently testing whether your UDP port is firewalled.

*Hidden*: The router is not configured to publish its address, therefore it does not expect incoming connections. Hidden mode is automatically enabled for added protection in certain countries. Too see the countries that are on this list refer to the Strict Countries List.

*WARN - Firewalled and Fast*: You have configured I2P to share more than 128KBps of bandwidth, but you are firewalled. While I2P will work fine in this configuration, if you really have over 128KBps of bandwidth to share, it will be much more helpful to the network if you open your firewall.

*WARN - Firewalled and Floodfill*: You have configured I2P to be a floodfill router, but you are firewalled. For best participation as a floodfill router, you should open your firewall.

*WARN - Firewalled with Inbound TCP Enabled*: You have configured inbound TCP, however your UDP port is firewalled, and therefore it is likely that your TCP port is firewalled as well. If your TCP port is firewalled with inbound TCP enabled, routers will not be able to contact you via TCP, which will hurt the network. Please open your firewall or disable inbound TCP above.

*WARN - Firewalled with UDP Disabled*: You have configured inbound TCP, however you have disabled UDP. You appear to be firewalled on TCP, therefore your router cannot accept inbound connections. Please open your firewall or enable UDP.

*ERR - Clock Skew*: Your system's clock is skewed, which will make it difficult to participate in the network. Correct your clock setting if this error persists.

*ERR - Private TCP Address*: You must never advertise an unroutable IP address such as 127.0.0.1 or 192.168.1.1 as your external address. Correct the address or disable inbound TCP on the Network Configuration page.

*ERR - SymmetricNAT*: I2P detected that you are firewalled by a Symmetric NAT. I2P does not work well behind this type of firewall. You will probably not be able to accept inbound connections, which will limit your participation in the network.

*ERR - UDP Port In Use - Set i2np.udp.internalPort=xxxx in advanced config and restart*: I2P was unable to bind to the configured port noted on the advanced network configuration page . Check to see if another program is using the configured port. If so, stop that program or configure I2P to use a different port. This may be a transient error, if the other program is no longer using the port. However, a restart is always required after this error.

*ERR - UDP Disabled and Inbound TCP host/port not set*: You have not configured inbound TCP with an address and port on the Network Configuration page, however you have disabled UDP. Therefore your router cannot accept inbound
connections. Please configure a TCP host and port on the Network Configuration page or enable UDP.

*ERR - Client Manager I2CP Error - check logs*: This is usually due to a port 7654 conflict. Check the logs to verify. Do you have another I2P instance running? Stop the conflicting program and restart I2P.

# I2P Applications, Services and Configuration

Applications are made available through a webUI, which listens at 127.0.0.1:7657.


# SusiMail 
![img](https://user-images.githubusercontent.com/50714166/188678059-289fe956-9c27-495a-bae2-7158ac010b84.png)

SusiMail is a secure email client. It is primarily intended for use with Postman’s email servers inside of the I2P network . It is designed to avoid leaking information about email use to other networks. SusiMail is bridged so it can send and receive email from the internet as well. Occasionally you may see some services like Gmail classifying it as spam, which you can correct in your Internet email service providers settings.

Postman’s service offers both internal and external email with POP3 and SMTP service through I2PTunnel. This allows people to use their preferred mail clients to send and receive mail pseudonymously.

Most mail clients expose substantial identifying information, however, SusiMail has been built specifically with I2P's anonymity abilities in mind. The I2Pmail/mail.i2p service offers transparent virus filtering as well as denial of service prevention with hashcash augmented quotas.
In addition, each user has control of their batching strategy prior to delivery through the mail.i2p outproxies, which are separate from the mail.i2p SMTP and POP3 servers. Both the outproxies and inproxies communicate with the mail.i2p SMTP and POP3 servers through I2P itself, so compromising those non-anonymous locations does not give access to the mail accounts or activity patterns of the user. More information can be found on the I2P Site: hq.postman.i2p.xyz.

SusiMail can be accesed from the router console. 
![img](https://user-images.githubusercontent.com/50714166/188678062-ca64d7fa-b511-4296-908f-94b7fbd28157.png)

# Snark
![img](https://user-images.githubusercontent.com/50714166/139136578-818c0cb8-f644-4e7f-9ba1-b5f950ea105e.png)

Snark is an I2P network only BitTorrent client. It never makes a connection to a peer over any other network.


# Static Site Template
![img](https://user-images.githubusercontent.com/50714166/139137278-85863a7f-e51d-47dc-ae94-95ac7345ca84.png)

A template that you can modify to set up your own self-hosted I2P site is included.


# The Address Book
![img](https://user-images.githubusercontent.com/50714166/139136086-a8759d09-9805-48b7-ba4f-453b263ac527.png)

This is a locally-defined list of human-readable addresses ( ie: i2p-projekt.i2p) and corresponding I2P addresses.(udhdrtrcetjm5sxzskjyr5ztpeszydbh4dpl3pl4utgqqw2v4jna.b32.i2p) It integrates with other applications to allow you to use those human-readable addresses in place of those I2P addresses. It is more similar to a hosts file or a contact list than a network database or a DNS service. There is no recognized global namespace, you decide what any given .i2p domain maps to in the end.


# The QR Code Generator
![img](https://user-images.githubusercontent.com/50714166/147276090-e8e2331c-95cf-415d-a123-a32b8ab26db9.png)

Besides the Address Book, I2P addresses can be shared by converting them into QR codes and scanning them with a camera. This is especially useful for Android devices.


# The Hidden Services Manager
![img](https://user-images.githubusercontent.com/50714166/147276313-9895a165-8ca1-4587-b55c-801d66bfce7b.png)

This is a general-purpose adapter for forwarding services ( ie SSH ) into I2P and proxying client requests to and from I2P. It provides a variety of “Tunnel Types” which are able to do advance filtering of traffic before it reaches I2P.


# Configuration/ Diagnostics
![img](https://user-images.githubusercontent.com/50714166/139135452-12b8a281-ae5a-4a0e-8efe-40da85fbe42c.png)

Customize your I2P router here. This includes bandwidth settings, home page, and the overall look and feel of your rouer console UI. Privacy and security setting can be adjusted here as well, such as your tunnel hops. Add more plugins and reseed from a url in this section as well.


# I2P Network Peers
![img](https://user-images.githubusercontent.com/50714166/188700328-2189440a-13ca-413f-9cc3-4d506a421765.png)

Check on Peer connections here, as well as UPnP Status.



