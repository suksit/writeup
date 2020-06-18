---
title: Phphonebook
subtitle: 100 Points
date: 2020-06-15T18:06:53+07:00
lightgallery: true
tags: [Web]
---

{{<image src="images/brief.png" caption="Brief">}}

{{<admonition warning Disclaimer>}}
To be honest I'm not very proud of this flag. I think I solved it by luck. I KNOW there is a more elegant way to do it, lol.
{{</admonition>}}

So after we follow the link we will reach this landing page.

{{<image src="images/landing-page.png" caption="Landing Page">}}

This looks very interesting to me -- it means that we should be able to do a local file inclusion (LFI) attack on this site. Let's keep that in mind for now...

{{<admonition quote>}}
Sorry! You are in /index.php/?file=

The phonebook is located at phphonebook.php
{{</admonition>}}

I try adding the `/phphonebook.php` to the URL and get this page.

{{<image src="images/phphonebook.png" caption="Phphonebook">}}

Posting some random data doesn't give anything interesting in the result page. So I just go back to the `/` path and try to do some LFI attacks.

Sadly, after almost an hour later, I'm out of my wit to think of a payload that works. So I go back to the `/phphonebook.php` page again and even re-read the hints in the brief:

{{<admonition quote>}}
... But you will get a flag only if it is an emergency!
{{</admonition>}}

I don't know what I was thinking back then but I add a hidden field named `emergency` with the value of `true` to the form, input some random number and then press Enter to submit it...

{{<image src="images/emergency-field.png" caption="Adding a Hidden `emergency` Field">}}

And that's how I got the flag when I wasn't really expecting it, lol.

{{<image src="images/flag.png" caption="A Random Flag Appeared!">}}

{{<admonition success Flag>}}
`flag{phon3_numb3r_3xtr4ct3d}`
{{</admonition>}}
