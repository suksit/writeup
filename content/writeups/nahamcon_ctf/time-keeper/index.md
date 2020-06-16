---
title: Time Keeper
subtitle: 50 Points
date: 2020-06-14T23:50:00+07:00
lightgallery: true
tags: [OSINT]
---

{{<image src="images/brief.png" caption="Brief">}}

So I followed the link and landed on this page:

{{<image src="images/apporima.png" caption="apporima.com">}}

After looking around the site for a while, including checking every posts, I didn't find anything useful for the flag. So I went back to the hint and this message just clicked:

{{<admonition quote>}}
Or at least, I thought **there was**...
{{</admonition>}}

If it's related to something in the past then the best place to find it is the [Wayback Machine](https://archive.org/web/). I typed `apporima.com` in the search bar and pressed Enter:

{{<image src="images/waybackmachine.png" caption="Wayback Machine for apporima.com">}}

There were 2 snapshots of the site -- one in May and the other in April. I started with May and the archived site looked pretty much the same as the current one, So I decided to go back further to April.

{{<image src="images/waybackmachine3.png" caption="Selecting April Snapshot">}}

The April snapshot showed a post that wasn't in the current site, and the post name was also interesting -- "Challenge Accepted!"

{{<image src="images/apporima-snapshot-april-2020.png" caption="April Snapshot of apporima.com">}}

After reading the post content, I was pretty sure this is it:

{{<admonition quote>}}
Today, I created my first CTF challenge. The flag can be found at forward slash flag dot txt.
{{</admonition>}}

So I added `/flag.txt` to the current URL and the flag appeared.

{{<image src="images/forward-slash-flag-dot-txt.png" caption="`/flag.txt`">}}

{{<admonition success Flag>}}
`JCTF{the_wayback_machine}`
{{</admonition>}}

{{<admonition info>}}
PS. I found out later that you can also get the flag by following the Github link at the top of the apporima.com page and looking for the repository of the site. The repo name is `apporima.github.io`. Then select branch `gh-pages` and from there you can browse the commit history and find the deleted `flag.txt` file.
{{</admonition>}}
