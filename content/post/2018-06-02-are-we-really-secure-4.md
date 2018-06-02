---
title: Bugs and Vulnerabilities 
subtitle: Are we really secure? (Part-4) - Understanding bugs and vulnerabilities 
date: 2018-06-02
bigimg: [{src: "/img/postimg/bugs.jpg", desc: "Security"}]
tags: ["hacking", "security"]
---
No matter how much time is devoted to developing an app or a website, or under how many eyes it passes through during its development stages, they still have vulnerabilities. 
Some have more so than others and some are just unusable. Every vendor on this planet has a security issue with their product. It has now become _a fact of modern-day life_.
Take Microsoft for instance. [CVE Details](https://www.cvedetails.com/top-50-vendors.php), a site that chronicles publicly disclosed vulnerabilities shows that in the 10 years starting with 2006 the company has disclosed an astonishing 3,157 security flaws.

While you might think that the developers are fighting it and you are not dealing with them directly, you cannot be more wrong. Active bug reporting is the key to a stable and secure product.

#### Technical Jargons
It is very important to introduce the terms that are used regarding security issues by the people working in the field, to avoid their overlapping and most of the time wrong usage.
You'll find many wrong usages of these terms, so here is a short list containing some commonly used terms. 

A **bug** is when a system is not behaving as intended. 

A **vulnerability** is a way to abuse a system most commonly it's regarding the security of that system.
A bug may introduce a vulnerability. 

An **exploit** is the realization of a vulnerability. It is a way which has already been invented after a vulnerability is known and the system can be exploited with it.

A **Zero-day threat** is a threat that exploits an unknown computer security vulnerability. Zero implies the developer’s ignorance of the exploit or bug. This means that there is no known security fix because developers are oblivious to the vulnerability or threat. 
A zero-day threat is also known as a _zero-hour attack_ or _day-zero attack_.

**CVE** - A [CVE](https://cve.mitre.org/cve) is a dictionary of publicly disclosed cybersecurity vulnerabilities and exposures that is free to search and use. It contains most of the known vulnerabilities to date.
Each entry into the list is assigned a CVE ID for reference like CVE-2014–6271.

![CVE](/img/cve.png)

**Patch** - It is the opposite of an exploit, it is a program that aims to fix the vulnerabilities.

The scale on which the tech giants work today is another major reason why even the smallest of vulnerabilities can be a real challenge for cybersecurity experts to solve overnight.
Or else, hackers can exploit them in a matter of seconds after they are known and are released to the public. As vulnerabilities always exist on a system at a given time, there is no way we can make sure that they are known to the public.
And when I say public, I mean developers and people working with the system, let alone the end users. Suppose if a Blackhat Hacker discovers the vulnerability first, then he may exploit it cleverly or worse, he can keep on bringing in hackers on board to exploit it and before the creators
know about it, its all out of their hands. 

While bugs and vulnerabilities cannot be entirely avoided on the developer's side, they can be pretty easily avoided on the end user's side. By simply updating the system, people can avoid disastrous bugs.
By just installing a 200KB update can actually save you from potential threats.

Another archive that is extensively used is [Exploit-DB](https://www.exploit-db.com) by Offensive Security. It is _"an archive of public exploits and corresponding vulnerable software, developed for use by penetration testers and vulnerability researchers"_.
It has a fairly large number of hacks and exploits and I love the way they categorize them, its easy enough to find what you want and I always use it for reference after a quick look at the target system. I recommend you to go ahead and give it a search for anything, like the phone you use or your router.

![Exploit-DB](/img/exploit-db.JPG)

Nowadays, you may hear about vulnerabilities in media too. You might have heard of _"Heartbleed"_, one of the most famous and the first bug that people went crazy over.
That is why they even named it and it even has a [website](http://heartbleed.com). Heartbleed, or the OpenSSL TLS 'heartbeat' Extension Information Disclosure Vulnerability (CVE-2014-0160), affects a component of OpenSSL known as Heartbeat. OpenSSL is one of the most widely used, open source implementations of the SSL (Secure Sockets Layer) and TLS (Transport Layer Security) protocols, the same "secure" protocols due to which this website that you are viewing is "https" encrypted, there is a green lock symbol too and it is said to be secure.
It allowed a hacker to attack any of the two-thirds of Web servers that used the OpenSSL and not merely remove its encryption, but force it to give up any random data from its memory, sensitive information such as login credentials, personal data, or even decryption keys. 
![Heartbleed](/img/heartbleed.png)
Another set of popular bugs and vulnerabilities like Shellshock, POODLE, Gotofail, and Ghost are patched to a large extent now and I am even talking about these because they are popular and they are popular because they have catchy names and an active [celebrity bug branding](https://medium.com/threat-intel/bug-branding-heartbleed-14ef1a64047f). 
Thousands of other bugs remain completely ignored by the media and the end-users.

While there is a whole community of cybersecurity experts, companies and users dedicated to building and providing patches for bugs. Be aware that not all bugs are fixed and there are always unknown bugs on any given system.

### Conclusion
As an end-user your role is minimal, but you should be aware of the scenario.

- Just download the latest update for your operating system, smartphone, router etc... and you should be fine. These updates patch most of the known vulnerabilities till the day they are released to the end users.

- Make sure you are not using a _super-old_ firmware on any of your devices, they are the ones which are affected severely during an outcry and its a hundred percent user's fault that they did not update it in time, despite the developer releasing them beforehand. 

#### Further Reading and Recommended Links - 
- [Exploit-DB](https://www.exploit-db.com) 
- [SC Magazine UK - Vulnerabilities](https://www.scmagazineuk.com/vulnerabilities/section/7018)
- [Vulnerability Magazine](https://www.vulnerability-db.com/?q=articles/vulnerabilities-bugs)
- [Detailed Database of Vulnerability Types](https://cwe.mitre.org/data/graphs/888.html)
- [Routerpwn - Exploits and Vulnerabilities for Routers](http://routerpwn.com/)