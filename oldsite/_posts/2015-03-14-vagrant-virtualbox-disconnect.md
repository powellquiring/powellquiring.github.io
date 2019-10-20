---
layout: post
title: vagrant creates a new virtualbox vm when the virtualbox home is not found
excerpt: The use of a flakey external drive is causing me problems with vagrant and virtual box.
tag:
 - docker
---
{{ page.excerpt }}

I ran out of disk space on c: so put my virtualbox Default Machine Folder on d:
The d: is a disk that slides into a device bay on my laptop that could alternatively house a battery, CD rom drive, ...
Sometimes after docking or undocking the d: is offline.
Vagrant up creates a new virtualbox vm with a similar name but different guid and provisions it.
Oh crap - i can reboot my computer to bring d: back online, but now the .vagrant directory is tied to the newly created image.
This is possible to fix up:

    $ cd C:\Program Files\Oracle\VirtualBox
    $ VBoxManage.exe list vms

find the guid of the bad and good vm.  In the .virtualbox directory there are 3 files that can be adjusted and one that can be deleted.

Alternatively take a look at this [post](http://www.psteiner.com/2013/04/vagrant-how-to-fix-vm-inaccessible-error.html) that I have not tried yet.
