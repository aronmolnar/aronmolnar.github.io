---
layout: post
title:  "Hacked in 30 minutes and 33 seconds"
author: Aron
date:   2021-06-16
description: I exposed a test system to the Internet. It took 30 minutes and 33 seconds to be compromised.
image: /assets/restricted.jpg
license: cc-by-4
---
###### I exposed a test system to the Internet. It took 30 minutes and 33 seconds to be compromised.

<img src="{{ "/assets/restricted.jpg" | relative_url }}" alt="restricted area" copyright="Pew Nguyen" />

Imagine you set up a server for testing and use weak credentials: Username "test" and password "test". Unfortunately, you expose the SSH port 22 to the public Internet by accident. Guess how long it would take until it is compromised!

I wanted to know and set up a honeypot system with an open SSH port. The first login attempt happened later than I expected. It took almost exactly 30 minutes until a client from Wyoming (USA) tried to log in using "esuser"/"esuser" (probably expecting an Elastic server). Ten seconds later, the attacker would have successfully logged in using "test"/"test". Our server would have been hacked after 30 minutes and 33 seconds.

<img src="{{ "/assets/honey.png" | relative_url }}" alt="honeypot logs with login attempts" />

Most attacks of this kind are presumably from malware that automatically tries to spread itself (worms). The malware would probably download its payloads from a remote server, start port scanning and brute-forcing other SSH services on the Internet. Before, it might do what it is built for: Steal your files, encrypt them to extort a ransom, install a crypto miner, be used as a jump host to hide the attacker's identity or other things.

In 24 hours, I observed attacks from 32 different IP addresses, most of them from the US (12) and China (7). There was a login attempt every 44 seconds on average, summing up to 1,950 total attempts and 869 unique username/password combinations. The most frequent credentials tried were "user"/"1" (20), "root"/"123456" (19), "admin"/"admin" (19) and "test"/"test" (17). 17 attackers would have been successful in taking over our server.

Even though the first login attempt took 30 minutes, the experiment shows how fast weak systems are hacked. This attack can easily be prevented by applying minimum security requirements like permitting remote authentication using certificates only (which should be the default on every system).

*You'll find all entered passwords on <a href="https://github.com/al3xdelarge/honeydata/blob/main/ssh_honeypot_passwords.tsv" target="_blank" rel="noopener">GitHub</a> under CC0 license.*
