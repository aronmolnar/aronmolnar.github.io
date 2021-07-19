---
layout: post
title:  "Detect hackers using canary tokens"
author: Aron Molnar
date:   2021-07-20
description: Canary tokens can be used to detect hackers easily. Without log correlation, AI, and even without blockchain. Usually, simple solutions are best.
image: /assets/mouse_trap.jpg
license: cc-by-4
---
###### Canary tokens can be used to detect hackers easily. Without log correlation, AI, and even without blockchain. Usually, simple solutions are best.

<img src="{{ "/assets/mouse_trap.jpg" | relative_url }}" alt="hacker touching mouse trap" copyright="Aron Molnar" />

In the past, canaries were taken into coal mines to detect carbon monoxide. When the birds fainted, miners left. Today, canary tokens (or honeytokens) might help you to detect attackers in an early stage.

Honeytokens are items that alert their usage. They might be email addresses (alert on received email, login attempt), credit cards (alert on tried debit), domain names (alert on resolve), web pages (alert on access), or files (alert on open). There are many more, of course.

Let's say we place an email address as a honeytoken into our customer database. Then we monitor for incoming emails and login attempts (e.g. via IMAP, SMTP, etc). Nobody should know this email address. Only if somebody gets access to our customer database, the honeytoken gets disclosed to the attacker. And if he then uses it (send a mail, try to log in) we can assume that our database was breached.

There are two problems with this scenario: Why should a hacker want to breach exactly this account of all? And more important: When somebody got his hands on our customer database, the worst case has probably just happened (we lost our customer data).

So let's place an email address and a pretended password into an HTML comment on our website. If we have many visitors there will probably be many people trying to (ab)use the honeytoken. What would we do if somebody did? You would only know that somebody has tried something without success. But what would be the subsequent action?

A honeytoken should be in a place where an attacker has already gained *some* privileges, but not *full* access. This might allow you to detect attackers, close potential vulnerabilities and issues of your perimeter (and network zones) and to start threat hunting in an early (but not too early) stage. This can be regarded as a rule of thumb. Of course, we also might want to know if an attacker has accessed our crown jewels.

My *rather no* places:
* An online shop's public section for registered customers (everybody could signup, customers have no elevated privileges)
* In the backend of an admin interface (already very high, or highest privileges)
* Somewhere only superusers or domain admins have access to

My *rather yes* places:
* Somewhere only paying customers have access to (maybe a customer account was compromised and now the attack continues?)
* Somewhere only low privileged staff has access to
* Somewhere only local admins have access to

Do you have honeytokens in place? I'd be interested in your experiences.