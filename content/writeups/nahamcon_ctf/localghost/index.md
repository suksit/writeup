---
title: Localghost
subtitle: 75 Points
date: 2020-06-15T17:06:53+07:00
lightgallery: true
tags: [Web]
---

{{<image src="images/brief.png" caption="Brief">}}

After following the link, we are greeted with a ghost ASCII art page that can be scrolled down indefinitely.

{{<image src="images/landing-page.png" caption="Ghost">}}

Viewing the page source doesn't show anything special...

{{<image src="images/view-source.png" caption="View Source">}}

There is a file named `jquery.jscroll2.js`, but its source is obfuscated... Maybe I'll come back to it later.

{{<image src="images/jscroll.png" caption="`jquery.jscroll2.js`">}}

Now I'm opening the inspector to see the DOM -- nothing interesting. JavaScript console also doesn't show anything suspicious. However, when I explore the storage tab. I get the flag in Local Storage section!

{{<image src="images/local-storage.png" caption="Local Storage">}}

{{<admonition success Flag>}}
`JCTF{spoooooky_ghosts_in_storage}`
{{</admonition>}}

{{<admonition info>}}
I found out later that you can also solve this by deobfuscating the code in `jquery.jscroll2.js` then you'll get an array named `_0xbcec`. There is a member named `flag` in the array and the one following it is a Base64 encoded string `SkNURntzcG9vb29va3lfZ2hvc3RzX2luX3N0b3JhZ2V9`. If you decode the string then you get the flag.
{{</admonition>}}
