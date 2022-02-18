---
layout: post
title:  "Help, my calls get intercepted!"
author: Aron Molnar
description: People often think that their communications are intercepted. Are they just paranoid or is something behind it?
date: 2021-09-09
image: /assets/cctv.jpg
license: cc-by-4
---
###### People often think that their communications are intercepted. Are they just paranoid or is something behind it?

<img src="{{ "/assets/cctv.jpg" | relative_url }}" alt="man on toilet with cctv" copyright="Aron Molnar" />

It was summer last year when I received a call from a friend who described a suspicion of a politician for EU in Brussels. Let's call that politician Bob. Bob suspected to be monitored. He has just talked to Alice on an international phone call. Alice said a sentence and a short time after, she repeated that sentence with the same intonation. Bob asked if she just really said that. She declined. Bob was certain that the call was recorded by a third party and replayed by accident during that phone call.

I asked some experts who might be able to unravel the mystery. The first reaction of one of the guys was like: "Was it an international call? Assume it was intercepted." A few weeks before, the German Constitutional Court (Bundesverfassungsgericht) ruled on the practice of untargeted bulk interception of the Federal Intelligence Service (Bundesnachrichtendienst, BND).

To make it short: The German BND intercepts up to 10% of all communications (including internet traffic, emails, phone calls, SMS) on 23 central exchange points, like DE-CIX in Frankfurt. Interception of German citizens is not allowed and is tried to be prevented by technical means (but does not work reliably). The court ruling did not forbid bulk interception per se but claimed more specific safeguards and more thorough supervision. The BND law must be repaired by end of 2021 but bulk interception will continue.

But what about Bob's phone record? If someone is wiretapping you, he must be very stupid to inject the record into your phone call. Here is a likely solution: An interconnection carrier connecting mobile providers cross-country replayed parts of the call to extend the duration of the phone call. This replay might result in discussions and will probably again extend the call. The longer the call takes, the more the interconnection carrier can charge.

It is not inspiring confidence to know about fraudulent interconnection carriers. Neither to know about wiretapping intelligence services. Both result in the same conclusion: Assume your unencrypted communication (including phone calls) is intercepted.

What to do about it?
* Use encrypted channels if it is confidential (default for any politician in Brussels; e.g. Signal or Threema for calls messaging)
* Make sure to use encrypted websites (https in the address bar)
* Make sure your emails are transferred encrypted to your office PC or mobile device
  * Prefer SSL/TLS over STARTTLS (but both is OK)
* Use S/MIME or PGP for end-to-end encryption of your emails

*A short note at the end*: If you are not an important politician, terrorist, hacker, dealer of weapons of mass destruction, <a href="{{ '/issues/they-have-full-access-to-your-phone-hacking-phones-with-zero-clicks' | prepend: site.baseurl }}" target="_blank">investigative journalist</a>, or something similar, I find it quite unlikely your communication is actively being monitored.

