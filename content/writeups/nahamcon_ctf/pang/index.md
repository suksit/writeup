---
title: Pang
subtitle: 40 Points
date: 2020-06-14T13:50:00+07:00
lightgallery: true
---

{{<image src="images/brief.png" caption="Brief">}}

So I downloaded the file and use `file` command and found that it's a PNG image.

{{<image src="images/file.png" caption="`file` command output">}}

The next thing I tried was `exiftool`.

{{<image src="images/exiftool.png" caption="`exiftool` command output">}}

No flag here. However, it showed some interesting warning:

{{<admonition warning>}}
[minor] Text chunk(s) found after PNG IDAT (may be ignored by some readers)
{{</admonition>}}

I wasn't sure what to do with this information so I tried `strings` to see if I could find that "text chunk".

{{<image src="images/strings.png" caption="`strings` command output">}}

No luck there either... So I went with another tool -- Stegsolve. Luckily, after opening the file in Stegsolve, it showed the flag:

{{<image src="images/stegsolve.png" caption="Opening `pang` File with Stegsolve">}}

{{<admonition success Flag>}}
`flag{wham_bam_thank_you_for_the_flag_maam}`
{{</admonition>}}

{{<admonition info>}}
PS. I found out later that if you download the file in Windows and just rename it to have `.png` extension, you can open the file and view the flag from Windows Explorer without any special tools.
{{</admonition>}}
