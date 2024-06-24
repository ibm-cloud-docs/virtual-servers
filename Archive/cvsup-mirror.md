---

copyright:
  years: 2014, 2017
lastupdated: "2017-09-29"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Archived 6/5/19 - cvsup mirror

We run a local cvsup mirror for you to update against. Make sure your supfile has the following entry:

*default host=cvsup.service.softlayer.com

We also mirror the distfiles available from freebsd.org, you can add the following line into your /etc/make.conf file to attempt to download from the local repository first:

MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"

If the file is not found there, it will follow the individual port Makefile and move to the next mirror.
