---
title: Read the Rules
subtitle: 5 Points
date: 2020-06-14T10:19:52+07:00
lightgallery: true
---

{{<image src="images/brief.png" caption="Brief">}}

So I followed the link and landed on this page:

{{<image src="images/rules-page.png" caption="Rules Page">}}

It explains everything regarding the CTF e.g.

* Don't attack the infrastructure
* You don't need automated scanners like `nmap`, `sqlmap`, etc.
* ...

It also explains the flag format, which is `flag{words_joined_together_with_underscore}`, and the most interesting thing it says would be:

{{<admonition quote>}}
If you look closely, you can even find a flag on this page!
{{</admonition>}}

Of course the first thing is to view the source. And there I found the flag near the `<footer>` section of the web page.

{{<image src="images/view-source.png" caption="View Source">}}

{{<admonition success Flag>}}
`flag{we_hope_you_enjoy_the_game}`
{{</admonition>}}
