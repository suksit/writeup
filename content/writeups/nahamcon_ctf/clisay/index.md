---
title: CLIsay
subtitle: 20 Points
date: 2020-06-14T10:19:53+07:00
lightgallery: true
---

{{<image src="images/brief.png" caption="Brief">}}

So I downloaded the file and executed it to see what it does.

{{<image src="images/execute.png" caption="Running `clisay`">}}

Hmm... It seems to be a relative of `cowsay` that won't say the thing we tell them to. I then tried using `stings` to see if there is anything interesting:

{{<image src="images/strings.png" caption="Output of `strings clisay`">}}

When I looked closely, I found two parts of the flag before and after the ASCII art.

{{<admonition success Flag>}}
`flag{Y0u_c4n_r3Ad_M1nd5}`
{{</admonition>}}
