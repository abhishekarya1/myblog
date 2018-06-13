---
title: A Brief Guide to Various Techniques in Hacking
subtitle: Understanding Hacking Techniques and Kali Linux Toolkit Overview  
date: 2018-06-13
bigimg: [{src: "/img/postimg/hacking_techniques.jpg", desc: "Hacking"}]
tags: ["hacking", "security"]
---

## Introduction

To be a Hacker, one has to be a master of multiple disciplines ranging from Operating Systems to Networking, and of course programming. They need to know everything about everything, from latest server technologies like Node.js to old programming languages like BASIC and C. They know almost every web framework, operating system, wireless technology, encryption that there is, in and out.

If you are finding weakness and loopholes in a system and gaining access or exploiting it then you are termed as a _Hacker_.
If you took prior permission from the owner then you are an _Ethical Hacker_ also known as _White Hat Hackers_ or _Penetration Testers_, if the access was unauthorized and unreported to the owner then you are called a _Black Hat Hacker_, and _Black Hat Hacking_ is a crime by law and such _Black Hats_ are criminals.
If you access in an unauthorized way and then report the loophole to the owner of the system to patch it, then you can be called a _Grey Hat Hacker_.

![Types of Hackers](/img/hackers.png)

A developer may be the best of his field but might know only about his field, the programming languages he use, the framework, or the OS he uses, but a hacker knows it better than him and a lot of other things, that too better than the programmer or developer. They even know it better than its creator because he needs to find vulnerabilities to exploit that the developer didn't had any idea about also called [Zero-Day Exploits](https://abyssaltech.xyz/post/2018-06-02-are-we-really-secure-4/).

At the most fundamental level, all Hackers weather ethical or black hat has to think alike, from the point of view of the black hat, because they often cause some hefty damages to system and it is important to think of the ways in which a black hat works.

Let us look at some of the techniques that hackers use to hack.

## Information Gathering

Gathering all kind of information about the target, as much as possible. 

The kind of information depends upon the target type. For Example -

If the target is an **Operating System** then the information about the boot method, or scheduler is important, 

If it is an **Android Device** then to which user it belongs to, what apps can are malicious, what is the version, etc... 

If it is a **Web Server** then what kind of OS does it use, what are available ports, and other specifications like protocol used, etc...

If it is a network like **Wi-Fi** then we often "map" the network - to create a visual map of the network including devices connected to it and total number of requests from a device, etc...  

Network and Port Scanning, Route Analysis, Live Host Identification are some examples.

**Reconnaissance** - [Google Hacking Database (GHDB)](https://www.exploit-db.com/google-hacking-database/), [WHOIS](https://whois.icann.org/en) and [DNStracer](http://www.mavetju.org/unix/dnstracer.php) are some examples of gathering data from online sources.

It is a very long process beause we need to familiarize ourselves with the target and then find loopholes by analyzing the collected data.

Also, do note that the target is not always a machine, it might be a person, or an organization like your college or office. Information gathering then requires the hacker to collect information like their schedule, data usage and even their habits.

## Vulnerability Analysis and Exploit Development

After everything about the target is known we proceed towards this phase where we check for known vulnerabilities and already known weaknesses of the target. Examples - if target is a network, we can check for known Router/Switch/Node vulnerabilities, or protocol related vulnerabilities, if it is a mobile device we can check for known vulnerabilities like overflow and apps with stray permissions that can be treated like hosts to carry out an attack.

If one wants to create exploits from scatch, most commonly used techniques that work on all targets are **Fuzzing** and **Stress Testing**. Feeding random inputs to the system with an intent to make it malfunction, or overflow the buffers.
With fuzzing, operating system kernels are exploited in the best way possible.

Another very popular stress test for websites and web servers id **DoS**(Denial of Service) attacks. We repeatedly send requests until the server is unable to handle them, eventually crashing it. 

Many of the security flaws come out after the fuzzing tests on systems that can be further used for exploit development.

Other examples include Stress Testing and Flooding.

## Web Application Analysis

A website is a place where the data flows in and out in substantial quantities. Data like passwords in the form of a request goes from the clients to the server and if the web app is not secure enough then the data will surely leak through and it can be intercepted by anyone on your network.

To check web apps, we can use various techniques like identification of CMS and backend - we can first find out what technologies are being used in the backend of a website and then proceed with Vulnerability Analysis on them.

Or we can use web vulnerability scanning that can help us identify vulnerabilities on a given webisite, or we can use Website Scraping to scrape data from a website directly.

Popular techniques of analysis include Mapping databases, Database Requests Framing, Web Based Auditing and Web Crawling and Scraping. 

## Database Assessment

Databases are everyehere. Databses store all kinds of information, the app information on your phone or your account information in the server, they even store files in cloud nowadays. So to hack those databses we have techniques like -

**Remotely accessing** the databases.

**Injection** - Injecting data into the database such that it accepts the wrong data as correct one, changing data in a databse by making it malfunction, 

**Brute Forcing** the passwords to a database - trying every possible password combination, 

**Mapping** the schema of the database remotely,

**Database Flooding** - Filling the databse with data until it malfunctions, and

**De-encrypting** the encrypted databases for data that they contain.

## Password Attacks

Passwords are everyhere too. To crack passwords we can use techniques like - 

**Dictionary Attacks** - To try passwords from a file that contains many passwords out of which one is right. 

**Brute Force Attacks** - To try every password combination specified by certain parameters like length and number of letters and numbers.

We can also find password loopholes like `sethc.exe` in Windows to bypass password entry and authentication completely.

**Hashing and Encryptions** - We can get an encrypted file that contains the password but is encrypted, we can then use **Reverse Hashing** and **Decryptors** to retrieve passwords.

**Password Profiling and Wordlists** - Sometimes we have to make our own worlists by analyzing the target, then we can gather information and profile passwords to atleast such an extent such that it reduces our bruteforce parameters.


## Wireless Attacks

Wireless technologies mainly include Wi-Fi, Infrared, and Bluetooth. They are easy to set up and use, but are mainly very insecure simply because they all **broadcast** packets of data through the air, where anyone can intercept them and extract data if they are not properly encrypted and in most case they are not.

**Cracking** - Discovering passwords from the network.

**Sniffing** - Collecting data from the network without intervening the connection.

**Spoofing/MITM/Phishing** -  Collecting data by sending spoofed requests, acting as a middleman between the user and the network itself and thus intercepting data that is meant for the server.

**Overflow** and **Router attacks** are applicable here too.

**Passive Sniffing (Wireshark)** - Sniffing packets off the air even when not connected to the network, we can then decode the packets to get data from them.

Mapping, ARP Spoofing, ARP Table overflow attack and SSL Stripping are the most commonly used attacks.


## Reverse Engineering and Code Reversing

Just like a real life machine can be opened up and modifications can be done to it, a software, program or a piece of code can be reverse engineered to such an extent that it can be modified or tested for vulnerabilities, or scanned for making exploits from it.

It is very difficult to successfully reverse engineer full source as coded by the developers from a given `.apk` or `.dll` library or an `.exe` as the compilers that created these were special ones like Dalvik Architecture Compilers for `.ODEX` files, and very often those compilers can be totally proprietary so no information is known to the reverse engineer.

Still reverse engineers leave no stones unturned to understand the functionalities and structure of the program to reverse engineer it. Furthermore, it requires a great deal of effort to understand the final result and underlying intricacies of the final reverse engineered source code to be able to fully utilize it.

**Smali** and **De-odexing** techniques are used for `.apk` and compilers such as `clang++` can be used to reverse engineer libraries written in C++. Also to help in the proceess and what is happenning behind the code, debuggers specially **Graphical Debuggers** can be used. 

## Exploitation

Exploiting the target system after we have developed an exploit is our focus here. How to get onto the system or network?, What data to collect?, How to send back harvested data? All of this is taken care of in the exploitation phase. Besides this target visualization,  Examples include -

Creating **Backdoors** - Malicious ways of entry into the system .e.g. bypassing the authentication.

Deploying **Payloads** - Payloads are nothing but programs that live on the target system and can be used to control the target and their data e.g. **RATs** and **Keyloggers**.

**Browser Payloads and Cookie Capturing/Stealing** - Payloads made for browsers and for stealing cookies from browsers that contain a lot of sensitive data.

**Honeypots** - Programs that monitor the system to identify intrusions and potential threats.

## Post Exploitation

To explore the system after exploitation, to generate logs and to maintain control of the target and harvesting data quietly, and password sniffing and cracking on the target system is called the post exploitation phase. For example -

After deploying a payload on Android we can make it hidden from the user to avoid getting detected, or after deploying a RAT onto a computer, we can use `Veil-Evasion` to avoid detection by an antivirus software.

**Privilege Escalation** - It is the most powerful and thus very common technique to escalate priviledges for the payload on the target system to prevent it from getting detected and eventually getting deleted or modified by the user, some other program or by the operating system itself.

## Forensics

TO analyze every possible kind of file that a hacker encounters. Be it checking PDF for malicious scripts or a JPEG for steganographic encodings, we may need to analyze every file of ours to avoid getting hacked ourselves, other examples include - 

**Browser Analysis** - Extracting every possible information from a browser like session information and user data.

**File Recovery** - Recovering deleted files to get information.

**Fingerprinting** - We can often find large data encoded in short bits called fingerprints and these fingerprints are used to refer to files from other files. We have to reverse trace our way to these large files using forensics on files where we found their fingerprints.

## Social Engineering

Deploying a payload needs much more skills than actually programming it! We need to make our payload believable, and user should accept it onto his system. 

**Payload Binding** works in most cases - it is binding the payload to the application that the target person likes and will readily download from the internet and use.

When making a wordlist we can use social engineering to get data.

**Phishing** - It is the one of those techniques that depends a lot on the use on social engineering, we have to create a webpage so believable that the user actually puts his credentials in the fake page from where we can harvest it.


## Reporting

Usually we end up with a lot of data after scanning and auditing, so for the purpose of reporting we enter the Reporting Stage. 

We have tools to prepare a log style report to package all of our collected data, or we can categorise it, for reference or for further testing or to submit to the owner of the system or to another penetration tester.  

## Conclusion

This was just an overview of some methods commonly used by hackers. I tried to make it as less technical as possible and this post will act as an introduction to my further posts on Hacking, Cybersecurity and Kali Linux.

## Learning Resources

Can't find any not technical one that covers everything above 😕.

Here is the Wikipedia [link](https://en.wikipedia.org/wiki/Security_hacker) though.

