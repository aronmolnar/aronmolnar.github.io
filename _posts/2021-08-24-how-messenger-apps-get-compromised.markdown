---
layout: post
title:  "How messenger apps get compromised"
author: Aron Molnar
description: "Messenger apps display an inconspicuous warning from time to time saying that a safety number has changed. This might not mean anything. It could mean everything."
date: 2021-08-24
image: /assets/phone_explosion.jpg
license: cc-by-4
---
###### Messenger apps display an inconspicuous warning from time to time saying that a safety number has changed. This might not mean anything. It could mean everything.

<img src="{{ "/assets/phone_explosion.jpg" | relative_url }}" alt="explosion behind a phone" copyright="Aron Molnar"  />

Most messengers that are end-to-end encrypted are based on a principle called "trust on first use" (TOFU). Encryption keys are exchanged the first time users are chatting. Whenever the underlying keys change, communications might have been compromised. This results in a warning by Signal. WhatsApp uses the same encryption protocol but does not display a warning by default. But what has happened?

**1. No breach: Your chat partner reinstalled his phone or got a new one**

This is the most probable scenario. Your chat partner reinstalled Signal. Device transfer (via Wi-Fi/Wi-Fi Direct) via Signal app prevents the change of safety numbers.

**2. Accidental breach: Your chat partner's number has changed**

Your chat partner got a new phone number. Someone else received his number from the provider and that's the person you are chatting with now. Your future messages are no longer secret (past messages remain secret).

Usually, telecom providers have a few months retention time for old numbers before assigning them to new customers.

**3. Intended breach: Stealing registration codes**

When you sign up for a messenger, you most often verify your phone number via SMS (or phone calls). There are hacker groups that trigger such a signup process which sends you the verification code. Afterwards, they call you and tell you a story, why you should provide them the signup code. If you do this, you are no longer the owner of your messenger.

It can also happen that somebody redirects your SMS messages to their phones. This can either be done by exploiting vulnerabilities in mobile networks, or by parking a car in front of your door and intercepting your mobile communications.

Another sneaky attack method is to ask the mobile provider for a new SIM card. An attacker might impersonate you and make your provider issue a new SIM card (e.g. because he claims he has lost his original SIM card). This is called SIM swapping.

In those cases, all future communications end up at the attacker's phone.
Your Signal peers would notice due to the warning they receive. WhatsApp peers will probably not notice at all.
You can impede account takeovers with Signal by enabling the registration lock option or with WhatsApp's two-step verification.

**4. Intended breach: Compromise of your messenger's server infrastructure**

Even if Signal's server infrastructure gets compromised, nobody can read your messages without changing the key material. Again, you would notice due to the change of the safety number. That's the cool thing about (real) end-to-end encryption.

One way to circumvent warnings is if an attacker can distribute a modified version of the messenger app. This modification could suppress the warnings and users would not notice the change of the key material.

Some messenger apps (like WhatsApp) backup your messages in plain text to your cloud provider. If an attacker gets access to your account, he will be able to access your messages in plain text, even if they were sent using end-to-end encryption.

**What to do about this**
* Enable <a href="https://faq.whatsapp.com/general/security-and-privacy/security-code-change-notification/" target="_blank" rel="noopener">Security Code Change Notification</a> on WhatsApp
* Enable registration lock (<a href="https://support.signal.org/hc/en-us/articles/360007059792-Signal-PIN#manage_registration_lock" target="_blank" rel="noopener">Signal</a>) or two-step verification (<a href="https://faq.whatsapp.com/general/verification/how-to-manage-two-step-verification-settings" target="_blank" rel="noopener">WhatsApp</a>) to prevent account takeover.
* Verify your contacts' safety numbers (<a href="https://support.signal.org/hc/en-us/articles/360007060632-What-is-a-safety-number-and-why-do-I-see-that-it-changed-#safety_number_view" target="_blank" rel="noopener">Signal</a>) and security codes (<a href="https://faq.whatsapp.com/general/security-and-privacy/end-to-end-encryption/" target="_blank" rel="noopener">WhatsApp</a>) when you meet them. Those contacts are then marked as verified and you can be sure to communicate with the right persons.
* Use a second channel to ask your contact why the safety number has changed (e.g. call him or write an email, SMS can be problematic).
* It is very suspicious if a peer's safety number changes several times in a row.
* If the safety numbers of all your peers change at the same time, something is really wrong.
* Do not backup your messages in plain text (Signal does not).

**Bonus: Your phone is fully compromised**

No "secure messenger" will keep your messages secret if your phone is compromised. Latest disclosures show that a spyware company can hack fully-patched phones without any user interactions by sending bogus messages. Fortunately, this software is sold to governments only. Unfortunately, <a href="{{ "issues/they-have-full-access-to-your-phone-hacking-phones-with-zero-clicks" | relative_url }}">governments monitor people not involved in serious crimes</a> (like journalists).

**What to do about this**

I will write an additional blog post about this and I will provide you a link here as soon as it is available.
