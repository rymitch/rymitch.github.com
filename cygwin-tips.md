---
layout: layout
title: Cygwin Tips
---

# Cygwin Tips

On Windows, I like to have a directory called `C:\Projects`
where my projects are stored.

Under [Cygwin](http://www.cygwin.com/) it is natural to map
this to `/Projects`. I know of two methods:

1. Use a symbolic link: `ln -s /cygdrive/c/Projects /Projects`

   This has the disadvantage that some tools will automatically
   expand the link for display. That means the ugly `/cygdrive/c`
   can sometimes show up when I don't want it to.

2. Use a mount point.

   This seems to be the most seamless way to integrate with
   the rest of the Cygwin envrionment. Edit `/etc/fstab` and
   add the following line:

         C:/Projects /Projects ntfs binary,posix=0 0 0

   Then issue the following command to refresh the current
   mount table:

         mount -a
