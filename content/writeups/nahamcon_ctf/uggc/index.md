---
title: UGGC
subtitle: 30 Points
date: 2020-06-14T13:50:00+07:00
lightgallery: true
---

{{<image src="images/brief.png" caption="Brief">}}

So I followed the link and landed on the `/login` page:

{{<image src="images/landing-page.png" caption="Login Page">}}

The brief says that I have to become the admin, so I tried putting "admin" in the username field. Of course it didn't work.

{{<image src="images/login-as-admin.png" caption="Try Logging in as admin">}}

Next, I tried logging in with username "ghost". It went through this time and I was redirected to `/` page with another error message.

{{<image src="images/login-as-ghost.png" caption="Try Logging in as ghost">}}

Now that it remembers my username. I should take a look at the cookie and see if I can modify it in order to become admin.

{{<image src="images/cookie-ghost.png" caption="ghost's Cookie">}}

There is a cookie named `user` with the value `tubfg`. It looks familiar but I'm not quite sure yet. So I tried logging in again with another username "uggc". This time the `user` cookie has the value of `http`.

{{<image src="images/cookie-uggc.png" caption="uggc's Cookie">}}

It looked like some kind of substitution cipher and the first thing that came into my mind was ROT13. So I went and check my assumption in CyberChef:

{{<image src="images/rot13-ghost.png" caption="ROT13 of ghost = tubfg">}}

Yep, my theory was right. So I just do ROT13 on "admin" and got "nqzva" then I went and replaced the value of the `user` cookie with it.

{{<image src="images/replaced-cookie.png" caption="Replaced Cookie Value">}}

After refreshing the page, I was greeted with the congratulations message and the flag.

{{<image src="images/logged-in-as-admin.png" caption="Successfully Logged in as admin">}}

{{<admonition success Flag>}}
`flag{H4cK_aLL_7H3_C0okI3s}`
{{</admonition>}}
