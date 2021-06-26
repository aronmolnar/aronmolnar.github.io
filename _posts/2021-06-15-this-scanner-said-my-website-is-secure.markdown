---
layout: post
title:  "This scanner said my website is secure..."
author: Aron Molnar
description: People often claim their website is secure because it got an "A" rating by a certain online scanner. This is often too simple.
image: /assets/open_door.jpg
date:   2021-06-15
license: cc-by-4
---
<img src="{{ "/assets/open_door.jpg" | relative_url }}" alt="open door with key" copyright="Andrea Piacquadio" />

###### People often claim their website is secure because it got an "A" rating by a certain online scanner. This is often too simple.
On the Internet, there are lots of great tools that make our lives easier.
However, it is important to understand what certain tools do. And what they don't.

One of those tools is the <a href="https://www.ssllabs.com/ssltest/analyze.html" target="_blank" rel="noopener">
"SSL Server Test" by Qualys</a>. It performs a great analysis
of a website's https settings. This is exactly what it does: It checks SSL/TLS settings. It actually does not check your 
website's *security*. Good crypto settings are, of course, part of security. But actually a very small part.

<img src="{{ "/assets/ssllabs.png" | relative_url }}" alt="ssllabs scanning result for securityguide.me (it got an A! :-) )" />

The SSL test does not look for outdated content management systems, plugins, config and debug files, or any other web vulnerability
like injections, broken authentication, etc. It gives a great report of your crypto settings.

I don't say crypto settings are not important. But a website is not secure just because it has great crypto settings.

The same applies to <a href="https://securityheaders.com/" target="_blank" rel="noopener">
securityheaders.com</a>. Security headers only play a role when the security maturity is high. They probably should be ignored 
by most companies, IMHO.
