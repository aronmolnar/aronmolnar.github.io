---
layout: post
title:  "Password complexity: How long it takes to crack passwords"
author: Aron Molnar
description: Find a set of illustrations how long it takes to crack passwords with different complexities.
date: 2021-11-02
image: /assets/billion_years.jpg
license: cc-by-4
---
###### The more complex and the longer a password is, the longer is the time to crack. This blog post illustrates how important it is to choose a long and complex password.

<img src="{{ "/assets/billion_years_run.jpg" | relative_url }}" style="border:2px solid #EEE;" alt="cracking duration simple passwords" copyright="Aron Molnar" />
A password with eight lower case characters allows 208 billion different combinations and can be cracked within two seconds. It takes as long as opening a letter.

If digits are used additionally, the cracking duration extends to 28 seconds, like a 200 meters sprint.

<img src="{{ "/assets/billion_years_meal.jpg" | relative_url }}" style="border:2px solid #EEE;" alt="cracking duration alphanumeric" copyright="Aron Molnar" />
If additional upper case characters are used, the cracking duration extends to 36 minutes, the duration of preparing lunch. The costs for a GPU server in the cloud are $0.60.

<img src="{{ "/assets/billion_years_flight.jpg" | relative_url }}" style="border:2px solid #EEE;" alt="cracking duration complex eight character passwords" copyright="Aron Molnar" />
If additional special characters are used, the cracking time extends from 36 minutes to 14 hours, like the duration of a flight from Paris to Sri Lanka. The cost: $14.

<img src="{{ "/assets/billion_years_summer.jpg" | relative_url }}" style="border:2px solid #EEE;" alt="cracking duration nine characters" copyright="Aron Molnar" />
With only one more character (nine instead of eight), the cracking duration is already 55 days, like school summer holidays in most countries. Costs rise to $1,300.

<img src="{{ "/assets/billion_years_dog.jpg" | relative_url }}" style="border:2px solid #EEE;" alt="cracking duration ten characters" copyright="Aron Molnar" />
Again, one more character (ten instead of nine) means that the cracking duration extends from 55 days to 14 years, the maximum lifetime of a dog. The costs for a GPU server in the cloud are $120,000.

<img src="{{ "/assets/billion_years.jpg" | relative_url }}" style="border:2px solid #EEE;" alt="cracking duration big bang passwords" copyright="Aron Molnar" />
14 characters mean that the cracking duration is at 1 billion years, the costs at $8,800,000,000,000.  
The big bang was approximately 13 billion years ago. One additional character (15) means that the cracking duration is at 91 billion years, the costs at $800,000,000,000,000.

### Some notes on the calculations
All calculations are based on the assumption that the passwords are generated randomly (like with a password manager). They are wrong if words from dictionaries or known passwords are used.

The calculations are based on MD5 hashes and a cracking rate of 100 Giga hash per second, which are easily achieved on a graphics card.  
More complex passwords hashing algorithms mean longer cracking durations (but the algorithm is not within the user's control; it might be MD5).  
Unsalted hashes can of course be cracked using rainbow tables, thus much faster (but they are feasible for up to approximately ten characters only).  
The price for a cracking server in the cloud is calculated at $1 per hour.

Even with a massive technology leap (like quantum computers), long and complex passwords are still to be regarded uncrackable. For example, a complex password with 14 characters can then be cracked in 91 million years instead of 91 billion years, which is still unfeasible and expensive.

Of course, cracking can be parallelized. While the time reduces linearly, the costs will remain (approximately).

### Video
<iframe src="//www.youtube.com/embed/BT94-f3zpFM" frameborder="0" allowfullscreen="" class="video" style="position: absolute;top: 0;left: 0;width: 100%;height: 100%;">
</iframe>