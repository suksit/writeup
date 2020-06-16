---
title: Metameme
subtitle: 25 Points
date: 2020-06-14T13:12:52+07:00
lightgallery: true
---

{{<image src="images/brief.png" caption="Brief">}}

So I downloaded the file. It was a JPG file of the meme from Mr. Robot.

{{<image src="files/hackermeme.jpg" caption="hackermeme.jpg">}}

Well first things first, I used `exiftool` to see the metadata of the image.

{{<image src="images/exiftool.png" caption="`exiftool` output">}}

And the flag is in the "Creator" attribute from the output above.

{{<admonition success Flag>}}
`flag{N0t_7h3_4cTuaL_Cr3At0r}`
{{</admonition>}}
