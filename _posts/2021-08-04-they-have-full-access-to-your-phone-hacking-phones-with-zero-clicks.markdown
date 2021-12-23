---
layout: post
title: "They have full access to your phone: Hacking phones with zero clicks"
description: "Security people, including myself, will need to rethink their recommendations: A spyware company hacking mobile phones for governments compromises fully patched phones without any user interaction. They come and go as they please and we don't even notice."
author: Aron Molnar
date: 2021-08-04
image: /assets/apple.jpg
license: cc-by-4
---
###### Security people, including myself, will need to rethink their recommendations: A spyware company hacking mobile phones for governments compromises fully patched phones without any user interaction. They come and go as they please and we don't even notice.

<img src="{{ "/assets/apple.jpg" | relative_url }}" alt="apple snacked by pegasus" copyright="Aron Molnar"  />

In December 2015, the FBI got their hands on a terrorist's iPhone. The terrorist killed 14 people in an attack in San Bernardino, California. Even though the phone was physically present in the hands of investigators, the FBI was unable to unlock it and access the data. After months, a company unlocked it for 900.000 US dollars. This looked like the moment of glory for mobile security.

More than five years later the disclosures of the "Pegasus Project", an investigative journalism initiative, have left me speechless. The spyware company NSO Group compromises fully patched iPhones (most likely Android phones too) without any user interaction ("zero-click") using their malware "Pegasus".

I am shocked that...

* there is nothing we can do to keep data on our phones secret and we would not even notice an infection.
* the exploits seem to work that good that the malware did not even persist. When agencies need access, they simply reinfect the phones.
* infected phones are fully remote-controlled, including microphone, camera, and keyboard (app).
* phones of at least 180 journalists from 21 countries were selected for surveillance.
* Pegasus malware was probably involved in the murders (Jamal Khashoggi, Cecilio Pineda) and imprisonments (Omar Radi, Anand Teltumbde) of journalists, and the capture of Princess Latifa.
* even democratic countries like Hungary seem to spy on domestic journalists (Szabolcs Panyi).
* NSO Group denies everything and apparently falsely claims that the malware "only collects data from the mobile devices of specific individuals, suspected to be involved in serious crime and terror".
* most people do not seem to care or notice.

The Pegasus Project questions many of the recommendations I gave in the past. I still think that it is a good idea to use encryption and strong passwords. But the offline world will be much more important for really secret information: Personal meetings and hand-written notes while shutting down our phones and storing them out of earshot.

<p style="margin:4rem;font-style:italic;">
"We've been recommending each other this tool or that tool, how to keep [our phones] more and more secure from the eyes of the government," Ismayilova said. "And yesterday I realized that there is no way. Unless you lock yourself in [an] iron tent, there is no way that they will not interfere into your communications." <sup>1</sup>
</p>

This exactly expresses my feelings right now: There is nothing we can do. And it will not go away. It might be that at some point in time, developers fix their issues and "zero-clicks" will (temporarily) disappear. But I believe that they will still find their way into our phones (even if we then have to click a link or so). And if they don't get you, they might get your friends, family, and peers.

I think that all people in IT security now must reflect and draw their conclusions. We (IT people) must be aware that we are responsible for our recommendations. Pegasus has proven that times in which you choose a strong passphrase and everything will be fine are over.

<br>
What are *your* conclusions? I would appreciate your response to <a href="&#x6d;&#x61;&#x69;&#x6c;&#x74;&#x6f;&#x3a;&#x61;&#x72;&#x6f;&#x6e;&#x40;&#x73;&#x65;&#x63;&#x75;&#x72;&#x69;&#x74;&#x79;&#x67;&#x75;&#x69;&#x64;&#x65;&#x2e;&#x6d;&#x65;">&#x61;&#x72;&#x6f;&#x6e;&#x40;&#x73;&#x65;&#x63;&#x75;&#x72;&#x69;&#x74;&#x79;&#x67;<!-- mail@example.com -->&#x75;&#x69;&#x64;&#x65;&#x2e;&#x6d;&#x65;</a>.


<br><br>
1. Phineas Rueckert at <a href="https://forbiddenstories.org/pegasus-the-new-global-weapon-for-silencing-journalists/" target="_blank" rel="noopener">https://forbiddenstories.org/</a>, Pegasus: The new global weapon for silencing journalists