---
title: Tron
subtitle: 75 Points
date: 2020-06-14T23:50:00+07:00
lightgallery: true
tags: [OSINT]
---

{{<image src="images/brief.png" caption="Brief">}}

Well there wasn't much info here. If it's a server then I think I should look the name up on popular sites... Here are the places I looked for him:

* https://www.facebook.com/nahamcontron -- :x:
* https://www.linkedin.com/in/nahamcontron -- :x:
* https://pastebin.com/u/nahamcontron -- :x:
* https://hackerone.com/nahamcontron -- :x:
* https://github.com/nahamcontron -- :heavy_check_mark:

{{<image src="images/github.png" caption="NahamConTron on GitHub">}}

Aha, so NahamConTron has a GitHub account. This sounds about right with the "Find his server" challenge. So I took a look at his repositories.

The `flagger` repo didn't have anything useful in the commits.

{{<image src="images/github-flagger.png" caption="NahamConTron's `flagger` repo">}}

I went to the other repo, `dotfiles`. The two latest commits looked very interesting since they're from JohnHammond and NahamConTron.

{{<image src="images/github-dotfiles.png" caption="NahamConTron's `dotfiles` repo">}}

NahamConTron's commit had nothing special. However, the commit by JohnHammond showed two very interesting things -- A bash history file that showed a `ssh` command along with the server address, username, and port. And the other file contains a OpenSSH private key:

{{<image src="images/johnhammond-commit.png" caption="Commit by JohnHammond">}}

Now that I found the server... I guessed I had to login to get the flag. So I downloaded the `id_rsa` file and tried it with the command showed in `.bash_history`

{{<image src="images/first-try.png" caption="SSH Key File Permission Error">}}

So it didn't work because the permissions of the key file was not correct. I had to change it to `-rw-------` or `0600` using `chmod`. Then I gave it another try -- this time I got in!

{{<image src="images/second-try.png" caption="Second Time's a Charm">}}

A quick `ls` showed there is a `flag.txt` file in the current directory, so I just `cat` it.

{{<image src="images/flag-txt.png" caption="Second Time's a Charm">}}

{{<admonition success Flag>}}
`flag{nahamcontron_is_on_the_grid}`
{{</admonition>}}
