---
title: Agent 95
subtitle: 50 Points
date: 2020-06-15T10:19:53+07:00
lightgallery: true
---

{{<image src="images/brief.png" caption="Brief">}}

Open the link and we are greeted with this page:

{{<image src="images/landing-page.png" caption="Landing Page">}}

It says that

{{<admonition quote>}}
You don't look like our agent!

We will only give our flag to our Agent 95! He is still running an old version of Windows...
{{</admonition>}}

So we need to change the HTTP User-Agent in order to get the flag. Let's try with something too obvious:

{{<image src="images/first-try.png" caption="Using `Agent 95` User-Agent">}}

Of course it doesnt' work, lol. So I googled for a browser User-Agent on Windows 95 and gave it another try. This time we get the flag.

{{<image src="images/flag.png" caption="Using a Windows 95 User-Agent">}}

{{<admonition success Flag>}}
`flag{user_agents_undercover}`
{{</admonition>}}
