---
layout: post
title:  "Can I report vulnerabilities to you?"
author: Aron
date:   2021-06-04
license: cc-by-4
---
# A security.txt file offers a great possibility to publish contact details of your security team.

If a security researcher finds a vulnerability or a data leak on the Internet, it is often not easy to find a contact person at the companies concerned. The researcher might not want to contact an office address without encryption. The email might pop up at a random person who is not concerned with security. This makes the reporting process cumbersome and the researcher might refrain from reporting the issue.

To solve this problem, there is the proposed standard of security.txt. This is a text file containg the contact details of the security team. You save them to your website in the web root or in the ".well-known" folder (better in both).

<img src="{{ "/assets/security_txt.png" | relative_url }}" alt="security.txt at BBC" />

The file can be easily generated at <a href="https://securitytxt.org/" target="_blank" rel="noopener noreferrer">securitytxt.org</a>.

Now, you receive security information for free. And life of idealistic and motivated security researchers is easier.

A security.txt file can be found at <a href="https://www.google.com/.well-known/security.txt" target="_blank" rel="noopener noreferrer">Google</a>, <a href="https://www.facebook.com/.well-known/security.txt" target="_blank" rel="noopener noreferrer">Facebook</a>, <a href="https://www.bbc.co.uk/.well-known/security.txt" target="_blank" rel="noopener noreferrer">BBC</a>, <a href="https://www.tesco.com/.well-known/security.txt" target="_blank" rel="noopener noreferrer">Tesco</a> and <a href="https://www.offensity.com/.well-known/security.txt" target="_blank" rel="noopener noreferrer">Offensity</a>.

Do you have experience in using a security.txt? I'd love to hear them.
