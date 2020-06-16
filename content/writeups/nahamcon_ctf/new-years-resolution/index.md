---
title: New Years Resolution
subtitle: 50 Points
date: 2020-06-14T23:50:00+07:00
lightgallery: true
---

{{<image src="images/brief.png" caption="Brief">}}

So I followed the link and landed on a blank page which kept loading... As the hint suggested there should be nothing on port 80 so I just focused on the phrase:

{{<admonition quote>}}
... old and deprecated nameserver technologies!
{{</admonition>}}

The first thing that came to my mind is it must have something to do with DNS records. So I started with `dig`:

{{<image src="images/dig.png" caption="`dig` output">}}

And the flag was there! To be honest, I didn't even know what an SPF record is... I looked it up later and found that it's Sender Policy Framework, which is some kind of email authentication method.

{{<admonition success Flag>}}
`flag{next_year_i_wont_use_spf}`
{{</admonition>}}
