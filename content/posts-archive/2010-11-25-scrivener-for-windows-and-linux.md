---
title: Scrivener for Windows… and Linux?
layout: post
date: "2010-11-25"
categories: [archive, broken_abbey]
---

There are some interesting things going on at
[Literature & Latte](http://www.literatureandlatte.com/). First, they've
released a Windows Beta version of their unique and popular writing software
[Scrivener](http://www.literatureandlatte.com/scrivener.php), which isn't really
news. However, what doesn't seem well-known yet is that on their message boards,
a group of folks is playing with an unofficial version for Linux.

If you're really interested in using Scrivener, I urge you to sign up for the
[Windows Beta](http://www.literatureandlatte.com/scrivenerforwindows/) and try
it out.
[Use Wine if you're Linux only](http://lifehacker.com/comment/31418541/). Also,
see the
[Linux user thread](http://www.literatureandlatte.com/forum/viewforum.php?f=30)
on L&L's forum. Sign up; help out. Finally, be aware that I do not give any
files directly in this post. I only link to files on L&L's forums.

This'll get you started, then once you're up and running head back to L&L's
message board for updates.

## Installation

I'm going to preface everything here with a quote from
[L&L's Blog, 13 Sept. 2010](http://www.literatureandlatte.com/blog/?p=133):

> ​10. Syncing for iPad, iPhone and Working Externally
>
> There's been a minor furor over my announcement that we currently don’t have
> any immediate plans for an iPad version, although an iPad version isn’t ruled
> out altogether in the long-term (other platforms that Scrivener won’t be
> coming to any time soon include Google Android, Linux and Commodore 64). But
> even without a dedicated app, Scrivener 2.0 provides some great ways for you
> to take your Scrivener documents with you for editing on an iPad or
> iPhone.(Emphasis mine).

This is all very unofficial. I use Ubuntu 10.10, i386 on my laptop and AMD64 on
my desktop, but this information should apply to other distros as well.

### Manual (i386 & AMD64)

See the Announcements on the
[Windows Bug Hunt](http://www.literatureandlatte.com/forum/viewforum.php?f=32)
forum for the latest Beta release. As of this writing, it's
[1.3](http://www.literatureandlatte.com/forum/viewtopic.php?f=32&t=9917).
Download the .zip file for Linux. I assume your download goes to ~/Download.

```bash
sudo unzip -d /tmp ~/Download/LinuxScrivenerBeta3.zip sudo
mv /tmp/LinuxScrivenerBeta3/LiteratureAndLatte /usr/local sudo ldd
/usr/local/LiteratureAndLatte/bin/Scrivener sudo chmod 755
/usr/local/LiteratureAndLatte/bin/Scrivener sudo rm -r /tmp/LinuxScrivenerBeta3
```

### Packages

[Randywallace](http://www.literatureandlatte.com/forum/memberlist.php?mode=viewprofile&u=9858)
has provided packages on the forum. The latest are available
[here](http://www.literatureandlatte.com/forum/viewtopic.php?f=30&t=9154&p=78141#p78141).
He provides deb, rpm, and tgz.

### Spell Checking

Spell checking worked for some but not others.

### i386

Make sure you have the libaspell and libaspell-devpackages installed. That's it.

### AMD64

Not so easy. It appearsthat Scrivener can't use the 64-bit aspell libraries.
But, it also seems that
[Opera had a similar issue on Ubuntu](https://help.ubuntu.com/community/OperaBrowser#32%20bit%20plugins).
Based on the Ubuntu help for Opera, I did the following:

Install libaspell and libaspell-dev from the repositories. This'll put the AMD64
versions on your system.

Download the i386 versions of
[libaspell](http://packages.ubuntu.com/maverick/libaspell15) and
[libaspell-dev](http://packages.ubuntu.com/maverick/libaspell-dev). If you're
not using Maverick, search for your release @ <http://packages.ubuntu.com>.
Again, I assume you downloaded to ~/Downloads.

```bash
cd ~/Downloads dpkg -x libaspell15_0.60.6-4ubuntu1_i386.deb
./libaspell dpkg -x libaspell-dev_0.60.6-4ubuntu1_i386.deb ./libaspell-dev
```

You have a choice now. You can install to Scrivener's lib directory:

```bash
sudo cp -d ./libaspell/usr/lib/libaspell*
/usr/local/LiteratureAndLatte/lib/ sudo cp -d ./libaspell-dev/usr/lib/libaspell*
/usr/local/LiteratureAndLatte/lib/
```

Or you can install to /usr/lib32 (which is what I did):

```bash
sudo cp -d ./libaspell/usr/lib/libaspell*/usr/lib32/
sudo cp -d ./libaspell-dev/usr/lib/libaspell*/usr/lib32/
```

In either /usr/lib32 or /usr/local/LiteratureAndLatte/lib, you should wind up
with:

```bash
-rw-r--r-- 1 root root 936 2010-11-24 16:19
/usr/lib32/libaspell.la lrwxrwxrwx 1 root root 19 2010-11-24 16:19
/usr/lib32/libaspell.so -> libaspell.so.15.1.4 lrwxrwxrwx 1 root root 19
2010-11-24 16:18 /usr/lib32/libaspell.so.15 -> libaspell.so.15.1.4 -rw-r--r-- 1
root root 603852 2010-11-24 16:18 /usr/lib32/libaspell.so.15.1.4
```

My original forum post is
[here](http://www.literatureandlatte.com/forum/viewtopic.php?f=30&t=9154&start=150#p79509).

# Install the Tutorial

The Linux zip file is provided without the Tutorial project. Here’s how you can
add it.This requires an install of the Windows Beta, either in Wine or on
Windows box:

1. In the Windows install, go to:C:\\Program Files\\Scrivener
2. In that directory, you’ll find a folder called:Tutorial.scriv
3. Copy that entire folder to the bin directory of your Linux Scrivener install.
   This might be /usr/local/LiteratureAndLatte/bin or /opt/scrivener_beta/bin
   depending on if you installed from scratch or used one of the packages from
   @randywallace.
4. Make sure theTutorial.scrivdirectory and all its files/subdirectories are
   owned by root: `chown -R root:root Tutorial.scriv`
5. Start Scrivener, go toHelp -\> Open Tutorial, and choose a place to save the
   Tutorial project.

Tutorial.scrivis not distributed in the Linux zip. I assume there's a good
reason, so do the above at your own risk.

Well, that's it for now. Enjoy!
