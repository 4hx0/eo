# How to downgrade Firefox on Ubuntu

So, you did an upgrade, and now Tab groups is no longer working in the rapid and ugly Firefox 57? Here's a simple way to reretrieve those groups, by temporarely downgrading Firefox: 

* Remove Firefox:

      sudo apt-get purge firefox

* Notice if it says that it's i-something-86 or amd64 that is deinstalling, or run:

      uname -a

  And check which you have.

* Download the older version, in this case 56, from this site – take the one closest corresponding to your architecture (i\*86 or amd64), the other wont work for your computer:

:https://sourceforge.net/projects/ubuntuzilla/files/mozilla/apt/pool/main/f/firefox-mozilla-build/

* Install it, assuming it's in a folder Download, which is default on English systems:

      sudo dpkg -i Downloads/firefox-mozilla-build_56.0.2-0ubuntu1_i386.deb

  or just:

      sudo dpkg -i Downloads/firefox[press tab and write alternatingly, until you find the right file]

Now, start Firefox, and (hopefully) enjoy your Tab group tabs.

## Comments

It has been said that this might not work if you've waited for too long after the upgrade, if you've used Firefox too much, in other words. You could look in to how to get a Firefox session back from the backups – in the meantime, do not use Firefox, or make a backup of your Firefox settings folder – it seems the session backups is stored in ~/.mozilla/firefox/[somestrangename]/sessionstore-backups. To backup all of it:

      cp -a .mozilla DOTmozilla-backup

The new and fancy way of writing apt-get is just "apt".

Since I don't have an English language version system, my default download folder is not called Downloads.
