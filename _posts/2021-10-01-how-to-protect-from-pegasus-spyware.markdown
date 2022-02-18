---
layout: post
title:  "How to protect from Pegasus spyware"
author: Aron Molnar
description: A spyware company hacks phones without user interaction. Can a phone be used without being monitored? Or do we have to accept that we cannot do anything against nation-state attacks? Let's disrupt the attack chain!
date: 2021-10-05
image: /assets/all_were_hacked.jpg
license: cc-by-4
---
###### A spyware company hacks phones without user interaction. Can a phone be used without being monitored? Or do we have to accept that we cannot do anything against nation-state attacks? Let's disrupt the attack chain!
<img src="{{ "/assets/all_were_hacked.jpg" | relative_url }}" alt="man crying" copyright="Aron Molnar" />

The NSO group hacked the iPhones of journalists without any user interaction using their malware Pegasus. They first sent a message to their victims via iMessage. iMessage accounts are either bound to phone numbers or email addresses. Governments need to know phone numbers or email addresses to compromise their targets' phones.

The messages contained malicious images. The images were processed by the iMessage app before the victims could have a look. Apps usually do not deliver their own image processing logic. They instead use operating system libraries (the camera app will use the same image processing library). The Pegasus malware exploited a vulnerability in the "ImageIO" library of iOS. They used a chain of multiple vulnerabilities to break out of the iMessage app and to completely take over the phone. This allowed the governments to access all other apps, private data, and also other system libraries, e.g. to access the camera, microphone, address book, or geolocation.

<img src="{{ "/assets/pegasus_infection.jpg" | relative_url }}" alt="Pegasus infection path" copyright="Aron Molnar" />

The biggest part of the attack chain takes place in software components provided by Apple. There are dozens of system libraries that probably contain security weaknesses. If a journalist wants to disrupt the attack chain, his only chance is to disrupt attackers at the beginning of the process. A government that does not know your phone number or email address will struggle to hack you.

However, this does not affect the iMessage app only. It might affect any inbound network traffic not limited to messaging: telecommunication signals, searching or downloading updates, synchronizing images or contacts, searching or connecting to Bluetooth devices, and fetching weather information. A vulnerability in iOS was recently disclosed that was triggered when the device connected to a Wi-Fi having a name containing percent symbols. Almost everything might be inbound traffic. Disabling apps, features and functionalities reduces the attack surface.

Even if most functionalities are disabled there will probably be a way into the phone if it is used for most common and regular tasks. Therefore, I suggest keeping your phone and harden it as well as you can. But you should still assume it is compromised (I call it "dirty phone"). Get a second phone and strip it down as much as possible and limit functionalities to the bare minimum. Use it for secret activities only. This is your "clean phone".

You might want to keep your dirty phone. If governments do not get their hands on your phone, they might place their bugs in your office and bedroom. In this case, I assume there is not much you can do against nation-state attacks.

*I started maintaining a [practical guide](https://github.com/aronmolnar/smartphone-hardening-guide) to instruct journalists how to set their phones. Contributions are warmly welcome.*