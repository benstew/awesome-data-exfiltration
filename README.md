# Awesome Data Exfiltration

> *Data exfiltration occurs when malware and/or a malicious actor carries out an unauthorized data transfer from a computer.* - Wikipedia

List of awesome, open source resources for data exfiltration to be used for educational purposes. Heavily influenced by https://attack.mitre.org/tactics/TA0010/

This is an evolving list so feel free to add more information via pull requests.

Table of Contents
=================

 * [Alternative Protocols](#-alternative-protocols)
 * [Automated Exfiltration](#-automated-exfiltration)
 * [Compressed Data](#-compressed-data)
 * [Command and Control Channels](#-command-and-control-channels)
 * [Data Transfer Size Limits](#-data-transfer-size-limits)
 * [Encrypted Data](#-encrypted-data)
 * [Other Network Mediums](#-other-network-mediums)
 * [Physical Mediums](#-physical-mediums)
 * [Scheduled Transfer](#-scheduled-transfer)
 * [Steganography](#-steganography)


## [↑](#table-of-contents) Alternative Protocols

Data exfiltration is performed with a different protocol from the main command and control protocol or channel. The data is likely to be sent to an alternate network location from the main command and control server. Alternate protocols include FTP, SMTP, HTTP/S, DNS, or some other network protocol. Different channels could include Internet Web services such as cloud storage.

#### Tools
* [DNSExfiltrator](https://github.com/Arno0x/DNSExfiltrator) Data exfiltration over DNS request covert channel

* [Egress-Assess](https://github.com/FortyNorthSecurity/Egress-Assess) Egress-Assess is a tool used to test egress data detection capabilities. Egress-Assess can send data over FTP, HTTP, and HTTPS.

* [PacketWhisper](https://github.com/TryCatchHCF/PacketWhisper) Stealthily exfiltrate data and defeat attribution using DNS queries and text-based steganography.

* [Pulsar](https://github.com/jacopodl/Pulsar) Data exfiltration and covert communication tool


## [↑](#table-of-contents) Automated Exfiltration

Data may be exfiltrated through the use of automated processing or scripting after being gathered during collection. When automated exfiltration is used, other exfiltration techniques likely apply as well to transfer the information out of the network, such as Exfiltration Over Command and Control Channel and Exfiltration Over Alternative Protocol.

#### Tools

* [PyExfil](https://github.com/ytisf/PyExfil): A Python Package for Data Exfiltration. Supports a ton of network, communication, physical, and steganography techniques.

* [Powershell-RAT](https://github.com/Viralmaniar/Powershell-RAT): Python based backdoor that uses Gmail to exfiltrate data through an attachment.

* [DET (extensible) Data Exfiltration Toolkit](https://github.com/PaulSec/DET): DET (is provided AS IS), is a proof of concept to perform Data Exfiltration using either single or multiple channel(s) at the same time. The idea was to create a generic toolkit to plug any kind of protocol/service to test implemented Network Monitoring and Data Leakage Prevention (DLP) solutions configuration, against different data exfiltration techniques.

* [SG1](https://github.com/evilsocket/sg1): A wanna be swiss army knife for data encryption, exfiltration and covert communication.


## [↑](#table-of-contents) Compressed Data

An attacker may compress data that is collected prior to exfiltration in order to make it portable and minimize the amount of data sent over the network. The compression is done separately from the exfiltration channel and is performed using a custom program or algorithm, or a more common compression library or utility such as 7zip, RAR, ZIP, or zlib.

#### Tools

* [zlib](https://github.com/madler/zlib): A massively spiffy yet delicately unobtrusive compression library.


## [↑](#table-of-contents) Command and Control Channels

Data exfiltration is performed over the Command and Control channel. Data is encoded into the normal communications channel using the same protocol as command and control communications.

#### Tools

* [DropFlop](https://github.com/pauln23/DropFlop) Use Dropbox as a command and control server. Perform data exfiltration.


## [↑](#table-of-contents) Data Transfer Size Limits

An adversary may exfiltrate data in fixed size chunks instead of whole files or limit packet sizes below certain thresholds. This approach may be used to avoid triggering network data transfer threshold alerts.

#### Tools
*


## [↑](#table-of-contents) Encrypted Data

Data is encrypted before being exfiltrated in order to hide the information that is being exfiltrated from detection or to make the exfiltration less conspicuous upon inspection by a defender. The encryption is performed by a utility, programming library, or custom algorithm on the data itself and is considered separate from any encryption performed by the command and control or file transfer protocol. Common file archive formats that can encrypt files are RAR and zip.

#### Tools

* [Badcookie](https://github.com/akbarq/Red-Team-Operations/blob/master/badcookie.py) exfiltrates data via base64 encoded HTTP cookies.


## [↑](#table-of-contents) Other Network Mediums

Exfiltration could occur over a different network medium than the command and control channel. If the command and control network is a wired Internet connection, the exfiltration may occur, for example, over a WiFi connection, modem, cellular data connection, Bluetooth, or another radio frequency (RF) channel. Adversaries could choose to do this if they have sufficient access or proximity, and the connection might not be secured or defended as well as the primary Internet-connected channel because it is not routed through the same enterprise network.

#### Tools
*


## [↑](#table-of-contents) Physical Mediums

In certain circumstances, such as an air-gapped network compromise, exfiltration could occur via a physical medium or device introduced by a user. Such media could be an external hard drive, USB drive, cellular phone, MP3 player, or other removable storage and processing device. The physical medium or device could be used as the final exfiltration point or to hop between otherwise disconnected systems.

#### Tools

* [CDitter](https://github.com/anfractuosity/cditter) A method for the exfiltration of data through the movement of a CD-ROM drive.


## [↑](#table-of-contents) Scheduled Transfers

Data exfiltration may be performed only at certain times of day or at certain intervals. This could be done to blend traffic patterns with normal activity or availability.

#### Tools
*


## [↑](#table-of-contents) Steganography

Hiding in plain site. Steganography is the practice of concealing messages or information within other non-secret text or data. There is a wide range of file types and methods of hiding files/data.

#### Tools

* [Cloakify](https://github.com/TryCatchHCF/Cloakify) Convert any filetype into list of everyday strings, using Text-Based Steganography.

* [spotexfil](https://github.com/sourcefrenchy/spotexfil) A simple attempt to exfiltrate data using spotify API, 300 bytes at a time. We can read a mini file (payload) and encode it inside a playlist description field via Spotify API. Really MVP/prototype, not meant for large files.

* [sneaky-creeper](https://github.com/DakotaNelson/sneaky-creeper) Using social media as a tool for data exfiltration.
