---
layout: post
title:  "Phones with Signal app should better not be investigated"
author: Aron Molnar
date:   2021-06-29
description: Developers of the Signal messenger app sow doubt in forensic investigation reports of mobile phones. One more reason why I really like Signal.
image: /assets/phones.jpg
license: cc-by-4
---
###### Developers of the Signal messenger app sow doubt in forensic investigation reports of mobile phones. One more reason why I really like Signal.

<img src="{{ "/assets/phones.jpg" | relative_url }}" alt="stack of mobile phones" copyright="Gabriel Freytez"  />

When investigators confiscate a mobile phone, they first need to unlock it for analysis. Otherwise, contents are often encrypted. Investigators might unlock devices using biometric marks, which can be enforced (e.g. face unlock, fingerprints, etc). If a passphrase is used only, the owner would need to disclose the secret for unlocking.

Another option is offered by professional investigation tools, like from the Israel-based forensic software provider Cellebrite. Cellebrite collects vulnerabilities and develops exploits to get access to the data and then copy and parse it.

The developers of the Signal messenger app somehow got their hands on a Cellebrite forensic kit ("*I saw a small package fall off a truck ahead of me*"). They started analyzing the software and - surprise - found a multitude of vulnerabilities in their parsing routines. If a malformed file is placed on a phone and then parsed by the forensic software, Cellebrite might either crash or even be compromised.

Signal developers not only demonstrated a fully functional exploit of the Cellebrite software but also say they can alter past and future data of other investigations (Multi-tenancy? What for?).

"*In completely unrelated news*", they write, future versions of Signal will "*be periodically fetching files to place*" on the device. "*These files are never used for anything inside Signal and never interact with Signal software or data, but they look nice, and aesthetics are important in software. Files will only be returned for accounts that have been active installs for some time already, and only probabilistically in low percentages*".

Signal might place files to mobile phones that could exploit forensic software and alter investigation reports. Even if those files do not actually exploit anything, it questions forensic reports massively.

Cellebrite will have difficulties in knowing if vulnerabilities are being exploited by the Signal app and if so, which vulnerabilities. "*We are of course willing to responsibly disclose the specific vulnerabilities we know about to Cellebrite if they do the same for all the vulnerabilities they use in their physical extraction*", Signal developers write.

In the meantime, Cellebrite announced to have resolved some security issues in a new version. They also dropped some functionalities for iOS devices. Probably due to a DLL included in their software to extract data from Apple devices that "*appear[s] to have been extracted from the Windows installer for iTunes*" (this might be quite problematic due to licensing issues).

There is nothing immoral in providing forensic software. What Signal blames Cellebrite for is to sell their software to "*death squads in Bangladesh*", "*military juntas in Myanmar*" and "*authoritarian regimes in Belarus, Russia, Venezuela, and China*". "*Their products have often been linked to the persecution of imprisoned journalists and activists around the world*".

<br>
*For more insights I recommend <a href="https://signal.org/blog/cellebrite-vulnerabilities/" target="_blank" rel="noopener">Signal's blog post</a>.*