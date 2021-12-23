---
layout: post
title:  "Communication during a hacker attack"
author: Aron Molnar
description: You cannot trust your office PC during a major incident. You can neither trust your usual communication and collaboration tools. If an attacker is able to authenticate on any domain-joined device with any domain user, game is over.
date: 2021-07-29
image: /assets/enigma.jpg
license: cc-by-4
---
###### You cannot trust your office PC during a major incident. You can neither trust your usual communication and collaboration tools. If an attacker can authenticate on any domain-joined device with any domain user, the game is over.

<img src="{{ "/assets/enigma.jpg" | relative_url }}" alt="enigma: break glass in case of cyber incident" copyright="Aron Molnar" />

Client-side encryption makes it difficult for attackers to exfiltrate massive amounts of data from central points. If all emails are end-to-end encrypted (e.g. using S/MIME or PGP done on office PC), an attacker cannot export them (in plain text) from the mail server.
Even if communication and collaboration tools are set up well and with great encryption, you cannot trust your office PC during a major incident. This is what companies could be prepared for.

Security teams and certain other teams (like top management) should not use their traditional toolset that is integrated into the corporate network during major incidents. Attackers could even steal encrypted files, chats, and emails when their devices are online. Threat hunting must not be done on potentially compromised (assume breach!) systems.

A toolset not integrated into the on-premise Active Directory (AD) could be prepared for certain employees. This might include a pool of notebooks, phones and SIM cards, conferencing tools, file shares, and an alternative email system.

Emergency notebooks must not be joined to the corporate network. However, access to the internal network should still be possible (e.g. for analysis). New phones are especially important if the old phones might be compromised via corporate mobile device management. Note that even "secure" messengers like Signal should not be used as always. Attackers might have got access to private keys, e.g. via desktop applications or compromised phones. If new SIM cards and phone numbers are available (maybe even from a different carrier), secure messengers can be freshly installed. Make sure to distribute address books containing the new phone numbers matched to your colleagues' names.

Client-side encrypted file shares, end-to-end encrypted chats, and a secure and an easy-to-use email solution could also be made available for the case of a major incident. I believe that these tools should be hosted solutions (Software-as-a-Service) for easy setup and prevention of misconfigurations and further security issues. Users should be used to the tools, if possible (e.g. replace Microsoft Teams with Microsoft Teams and different AD tenant).

It is also part of good preparation to involve the purchasing department to be able to swiftly acquire additional software or hardware in case of emergency. However, a basic toolset might already be purchased upfront.

Here are some tools I made good experiences with:

* File shares
  * [Tresorit](https://tresorit.com/)
  * [Nextcloud](https://nextcloud.com/)
* Communication tools
  * [Microsoft Teams](https://www.microsoft.com/en-ww/microsoft-teams/group-chat-software)
  * [Signal](https://signal.org/)
* Email services
  * [mailbox.org](https://mailbox.org/)
  * [ProtonMail](https://protonmail.com/)
  
Do you have some additional recommendations?