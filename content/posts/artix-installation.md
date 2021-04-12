---
title: "101.Artix"
date: 2021-04-12T10:07:34+03:00
draft: false
tags: ["101", "artix", "installation"]
---


**[Artix](https://artixlinux.org/)** [The Art of Linux] - systemd-free GNU/Linux distribution. It uses OpenRC, runit or s6 as init system.

Basically, it's fork of the Arch with minimal differences, it's almost the same, but there is an option of runit system (due to it, few Arch packages might not be available yet). 

Below I'll put link. There are you find external links and information against systemd, and why you should use Artix Linux or similiar distributions:

* [no systemd](https://nosystemd.org/) - website tries to become a collection of resources pointing out reasons against systemd and what alternatives are available.

In default, Artix Linux mirrors have some .iso with preinstalled DE, it's simplifies installation for begginer users due to contained GUI installer.

But, I doesn't like Calamares installer at all, it's make the same work as manual installation, but it very limited in options.

Here's, instruction of installation (hope, it'll be useful for you as well as for me):

---

**Note**

* ignore all lines after <-, I used it as comments.

**Set the keyboard layout**

```sh
# ls /usr/share/kbd/keymaps/**/*.map.gz <- check available layouts
# loadkeys key de-latin1 <- optional, in this case, set German keyboard layout
```

**Connect to WIFI**

```sh

```

Work-in-Progres ...
