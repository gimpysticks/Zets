---
title: issue
created: 2025-10-21
modified: 2025-10-21
---

USER:
Password for 'https://gimpysticks@bitbucket.org': 
remote: You may not have access to this wiki or it no longer exists in this workspace. If you think this wiki exists and you have access, make sure you are authenticated.
fatal: Authentication failed for 'https://bitbucket.org/gimpysticks/zets.git/wiki/'

AGENT:
I see you're having an authentication issue with a Bitbucket wiki repository. The error message indicates either:

1. **Authentication failure** - Your credentials aren't working
2. **Access permissions** - You don't have access to this wiki
3. **Wiki doesn't exist** - The wiki may have been deleted or moved

Let me help you troubleshoot this. First, let's check what's happening with your git operation:

**Command Executed:**
```bash
git remote -v
```

**Output:**
```
fatal: not a git repository (or any of the parent directories): .git
```

It looks like you're not in a git repository currently. Let me check if there's a zets directory and what's in it:

**Command Executed:**
```bash
ls -la
```

**Output:**
```
total 5216184
drwx------ 438 sticks sticks      36864 Oct  9 01:19  .
drwxr-xr-x   3 root   root         4096 Sep 21 14:49  ..
-rw-rw-r--   1 sticks sticks          0 Aug 31  2023 '<'
-rw-rw-r--   1 sticks sticks       2722 Jul 19  2024  1814262060366053379
-rw-r--r--   1 sticks sticks     825170 Oct 17  2019  1_Meadowood_Greene.pdf
-rw-rw-rw-   1 sticks sticks  200716110 Apr 23  2023 '2023-04-23 22-04-57.mkv'
-rw-r--r--   1 sticks sticks     757208 Aug  8  2023 '2023-08-08 01-21-01.mkv'
-rw-rw-r--   1 sticks sticks    5016292 Mar 13  2024 '2024-03-13 11-15-31.mkv'
-rw-r--r--   1 sticks sticks   37509006 Jun 17  2024 '2024-06-17 18-43-57.mkv'
drwx------   2 sticks sticks       4096 Aug 31 04:15  2FA_QRCode_Images
-rw-rw-r--   1 sticks sticks        783 Feb 14  2024  2manywizards
drwx------   2 sticks sticks       4096 Aug 31 04:15  3LadiesThai
lrwxrwxrwx   1 sticks sticks         81 Oct 31  2023  aces -> '/home/sticks/.steam/debian-installation/steamapps/common/War Thunder/linux64/aces'
-rw-r--r--   1 sticks sticks        793 Jun 24  2019  .acidriprc
-rwxr-xr-x   1 sticks sticks    9469015 Jun 24  2019  adltpl
drwx------   6 sticks sticks       4096 Nov  6  2019  .adobe
-rw-------   1 sticks sticks         32 Aug 31  2021  adoptopenjdk-keyring.gpg~
lrwxrwxrwx   1 sticks sticks         11 May  4  2020  adult -> /mnt/adult/
-rwxrwxrwx   1 sticks sticks        385 May 26  2023  adult_term
drwx------   2 sticks sticks       4096 Aug 31 04:15  advancements
-rw-rw-r--   1 sticks sticks        927 Apr 12  2021  Afishionados.csv
-rw-rw-rw-   1 sticks sticks       4246 Jun  8  2023  .alias
drwx------   2 sticks sticks       4096 Aug 31 04:15  Amanda_Files
-rwxr-xr-x   1 sticks sticks         63 Aug 14  2020  amazing.python1.py
drwx------   2 sticks sticks       4096 Feb 15  2023  .amazonmp3
-rw-rw-r--   1 sticks sticks       1458 Feb 20  2024  ambrotype_synthwave
drwx------   3 sticks sticks       4096 Jan 17  2020  .android
drwx------   2 sticks sticks       4096 Aug 31 04:15  apache-maven-3.6.0
-rw-rw-r--   1 sticks sticks    5915004 Dec  6  2021  appimagelauncher_2.2.0-travis995.0f91801.bionic_amd64.deb
drwx------   2 sticks sticks       4096 Oct  8 22:36  Applications
-rw-r--r--   1 sticks sticks        276 Jun 24  2019  .apport-ignore.xml
drwx------   2 sticks sticks       4096 Jan  6  2019  .aptitude
-rw-r--r--   1 sticks sticks   36669817 Aug 18  2016  Aquatic_Jambiance.flac
-rw-rw-r--   1 sticks sticks    4979602 Jul  5  2023  Aquatic_Jambiance.flac.ogg
-rw-r--r--   1 sticks sticks       4205 Jun 24  2019  arco_keybindings.txt
-rw-rw-r--   1 sticks sticks      69439 Jul  5  2023  arco_keybindings.txt.ogg
drwxr-xr-x   2 sticks sticks       4096 Jun 24  2019  .arcolinux-logo
-rw-rw-r--   1 sticks sticks          0 Sep 22 16:01  as
-rw-r--r--   1 sticks sticks         86 Jun 24  2019  .asoundrc
-rw-r--r--   1 sticks sticks         24 Aug 17  2020  .aspell.en.prepl
-rw-r--r--   1 sticks sticks         43 Aug 17  2020  .aspell.en.pws
drwx------   2 sticks sticks       4096 Aug 31 04:15  assets
-rw-r--r--   1 sticks sticks        159 Jun 24  2019  .asunder
-rw-r--r--   1 sticks sticks         17 Jun 24  2019  .asunder_album_artist
-rw-r--r--   1 sticks sticks          5 Jun 24  2019  .asunder_album_genre
-rw-r--r--   1 sticks sticks          9 May 26  2014  .asunder_album_title
drwxr--r--   2 sticks sticks       4096 Mar  8  2020  .att_backups
drwxr--r--   2 sticks sticks       4096 Feb 17  2020  .att_Backups
drwxr-xr-x   2 sticks sticks       4096 Feb  6  2020  .ATT_Backups
drwx------  10 sticks sticks       4096 Jun 24  2019  .attract
-rw-rw-r--   1 sticks sticks        124 Feb 20  2025  attributions.txt
-rw-------   1 sticks sticks       1508 Apr 18  2020  audacity_play.aup
drwx------   2 sticks sticks       4096 Aug 31 04:15  audacity_play_data
drwx------   2 sticks sticks       4096 Oct  8 13:22  Audio
lrwxrwxrwx   1 sticks sticks         32 Sep 26 19:08  .authorizations -> /home/sticks/bin/.authorizations
drwx------   2 sticks sticks       4096 Aug 31 04:15  autopy
drwx------   3 sticks sticks       4096 Jun 24  2019  .avidemux
lrwxrwxrwx   1 sticks sticks         12 Oct 30  2019  backup -> /mnt/backup/
drwx------   2 sticks sticks       4096 Aug 31 04:15  backups
-rw-r--r--   1 sticks sticks        341 Apr 14  2024  backup.tmp
-rw-r--r--   1 sticks sticks     806541 Jun 24  2019  bandcamp.xcf
-rw-rw-r--   1 sticks sticks          2 Feb 16  2023  banned-ips.json
-rw-rw-r--   1 sticks sticks          2 Feb 16  2023  banned-players.json
-rw-rw-r--   1 sticks sticks     970789 Oct 28  2024  baron.m4a
lrwxrwxrwx   1 sticks sticks         28 Dec 17  2021  .bash_aliases -> .dotfiles/bash/.bash_aliases
drwx------   2 sticks sticks       4096 Aug 31 04:15  Bash_Basics
-rw-------   1 sticks sticks      36331 Jun  3 20:36  .bash_history
-rw-r--r--   1 sticks sticks        220 Sep 15  2020  .bash_logout
-rw-r--r--   1 sticks sticks         79 Apr 15  2024  .bash_profile
lrwxrwxrwx   1 sticks sticks         22 Dec 17  2021  .bashrc -> .dotfiles/bash/.bashrc
-rw-r--r--   1 sticks sticks       5563 Jan  8  2020  .bashrc-copy
lrwxrwxrwx   1 sticks sticks         30 Dec 17  2021  .bashrc_history -> .dotfiles/bash/.bashrc_history
lrwxrwxrwx   1 sticks sticks         31 Dec 17  2021  .bashrc-personal -> .dotfiles/bash/.bashrc-personal
drwx------   2 sticks sticks       4096 Aug 31 04:15  bashscripts
drwx------   2 sticks sticks       4096 Aug 31 04:15  Bash-Snippets
-rw-r--r--   1 sticks sticks      14785 Jan  4  2020  BDLL-01-04-20_1949.txt
-rw-rw-r--   1 sticks sticks     140839 Jul  5  2023  BDLL-01-04-20_1949.txt.ogg
-rw-r--r--   1 sticks sticks      41886 Aug 22  2020  BDLL-08-22-2020.txt
-rw-rw-r--   1 sticks sticks     306449 Jul  5  2023  BDLL-08-22-2020.txt.ogg
-rw-r--r--   1 sticks sticks       1074 Jul 13  2019  BDLLEnd
-rw-r--r--   1 sticks sticks     347965 Jun 24  2019  Bedroom-packages
-rw-rw-r--   1 sticks sticks  201930607 Sep 22 10:09  Beeper-4.1.186.AppImage
-rw-rw-r--   1 sticks sticks   11749978 Aug 24  2024  BeerBrakcet_2020.png
-rw-rw-r--   1 sticks sticks     107285 Jul  5  2023  BeerBrakcet_2020.png.ogg
-rw-rw-r--   1 sticks sticks         96 Mar 31  2018  ben10
drwx------   2 sticks sticks       4096 Aug 31 04:15  Biddle_vim
drwxr-xr-x   4 sticks sticks       4096 Apr 25  2020  .bin
drwxrwxr-x   9 sticks sticks      20480 Oct  6 03:00  bin
lrwxrwxrwx   1 sticks sticks         51 Nov 17  2023  bin32 -> /home/sticks/.steam/debian-installation/ubuntu12_32
lrwxrwxrwx   1 sticks sticks         51 Nov 17  2023  bin64 -> /home/sticks/.steam/debian-installation/ubuntu12_64
drwx------   2 sticks sticks       4096 Aug 31 04:15  binfiles
-rw-rw-r--   1 sticks sticks     663851 Aug 24  2024  bitmap.png
-rw-r--r--   1 sticks sticks     191729 Dec 15  2019  bitwarden_export_20191215122715.json
srw-------   1 sticks sticks          0 Sep 20 16:33  .bitwarden-ssh-agent.sock
drwx------   2 sticks sticks       4096 Dec 20  2018  .bl2
-rw-rw-r--   1 sticks sticks     500655 Aug 24  2024  Black_GS_Logo.png
-rw-rw-r--   1 sticks sticks       4698 Jul  5  2023  Black_GS_Logo.png.ogg
drwx------   3 sticks sticks       4096 May 20  2012  .blender
-rw-rw-r--   1 sticks sticks     193744 Dec 19  2020  bluegrass_backstabber.svg
-rw-rw-r--   1 sticks sticks      19781 Jul  5  2023  bluegrass_backstabber.svg.ogg
-rw-rw-r--   1 sticks sticks     281574 Apr  6  2025  bookmarks-2025-04-06.json
-rw-rw-r--   1 sticks sticks     512949 Aug 24  2024  brcc.png
-rw-rw-r--   1 sticks sticks      10075 Jul  5  2023  brcc.png.ogg
drwx------   2 sticks sticks       4096 Aug 31 04:15  BuildData
-rw-rw-r--   1 sticks sticks       1267 Feb 16  2023  bukkit.yml
drwx------   3 sticks sticks       4096 Jul  5  2024  .byobu
-rw-r--r--   1 sticks sticks        980 Jun 24  2019  .bzr.log
drwx------  47 sticks sticks       4096 Oct  5 00:20  .cache
drwx------   2 sticks sticks       4096 Aug 31 04:15  cache
-rw-------   1 sticks sticks        133 Jun 24  2019  .calc_history
drwxr-xr-x   5 sticks sticks       4096 Oct  1 23:01  .cargo
-rw-rw-r--   1 sticks sticks     158301 Jan 11  2019  cathedral-bazaar_djvu.txt
-rw-rw-r--   1 sticks sticks     760532 Jul  5  2023  cathedral-bazaar_djvu.txt.ogg
-rw-r--r--   1 sticks sticks   36403764 Jun 24  2019  Cayde-Dugout.mov
-rw-rw-r--   1 sticks sticks      15824 Jul  5  2023  Cayde-Dugout.mov.ogg
drwx------  13 sticks sticks       4096 May  4  2014  .cddbslave
-rw-rw-r--   1 sticks sticks      10110 Jun 24  2019  celeb.pdf
drwx------   2 sticks sticks       4096 Aug 31 04:15  cell
drwx------   2 sticks sticks       4096 Aug 31 04:15  cepstral_Voices
drwxr-xr-x   3 sticks sticks       4096 Sep 24  2021  .cert
drwx------   2 sticks sticks       4096 Aug 31 04:15  cfg
-rw-rw-r--   1 sticks sticks          0 Jun 30 07:15  chatgpt_content.md
drwx------   2 sticks sticks       4096 Jan  6  2017  .cheat
drwx------   2 sticks sticks       4096 Aug 31 04:15  cheat
drwx------   2 sticks sticks       4096 Aug 31 04:15  cheat.sh
-rw-r--r--   1 sticks sticks    3337834 Dec 21  2016  chromedriver_linux64.zip
-rwxr-xr-x   1 sticks sticks        312 Aug 10 19:03  chrome-jhjcdofpkbdhhdfaemgoohfffcfiggpe-Default.desktop
-rwx------   1 sticks sticks         49 Mar  8  2016  .chrome-remote-desktop-session
drwx------   2 sticks sticks       4096 Aug 31 04:15 'Cincinnati Air Traffic Control (@cvg_atc) • Instagram photos and videos_files'
-rw-rw-r--   1 sticks sticks          0 Aug 24  2024  cinfed.png
-rw-r--r--   1 sticks sticks      57993 Nov  6  2019  cinfed.png~
drwx------   5 sticks sticks       4096 Jun 24  2019  .cinnamon
drwx------   4 sticks sticks       4096 Jun 24  2019  .clamz
-rw-r--r--   1 sticks sticks       3367 Jun 24  2019  class76NotFound.txt
-rw-r--r--   1 sticks sticks       8272 Jun 24  2019 'Class roster with missing 2015.txt'
drwxrwxr-x   5 sticks sticks       4096 Jul 13 15:43  .claude
-rw-rw-r--   1 sticks sticks      15230 Jul 13 15:46  .claude.json
-rw-rw-r--   1 sticks sticks      14855 Jul 13 15:46  .claude.json.backup
-rw-rw-r--   1 sticks sticks       3456 Jun 30 18:43  CLAUDE.md
drwx------   8 sticks sticks       4096 Feb 15  2023  .claws-mail
drwxr-xr-x   3 sticks sticks       4096 Feb 28  2019  .cmake
-rw-rw-r--   1 sticks sticks        182 Apr  5  2022  Coinbase_2021_Gain_Loss.csv
-rw-r--r--   1 sticks sticks       7189 Jun 24  2019  colby_cheeze_vimrc.txt
-rw-rw-r--   1 sticks sticks      17215 May  1 03:27  combined-packages.txt
-rw-r--r--   1 sticks sticks        288 Jun 24  2019  .comex-base.xml
-rw-rw-r--   1 sticks sticks         40 Jul  6  2022  commands
-rw-rw-r--   1 sticks sticks        202 Mar  5  2025  .commands.json
-rw-rw-r--   1 sticks sticks         31 Mar  5  2025  commands.json
-rw-rw-rw-   1 sticks sticks       4036 Jun 24  2023  com.valvesoftware.Steam.flatpakref
drwx------ 397 sticks sticks      20480 Oct  9 00:15  .config
drwx------   2 sticks sticks       4096 Aug 31 04:15  config
-rw-r--r--   1 sticks sticks       7050 Apr 26  2020  .conkyrc
-rw-r--r--   1 sticks sticks       1544 Feb 16  2023  .console_history
-rw-rw-r--   1 sticks sticks     919656 Jun 20 11:15  cover.jpg
-rw-rw-r--   1 sticks sticks       7138 Jan  5  2021  covid_Text.svg
drwx------   2 sticks sticks       4096 Aug 31 04:15  cozmo-python-sdk
drwx------   2 sticks sticks       4096 Aug 31 04:15  CraftBukkit
drwx------   2 sticks sticks       4096 Aug 31 04:15  crash-reports
-rw-r--r--   1 sticks sticks      71727 Nov  7  2019  crutch1.png
-rw-r--r--   1 sticks sticks      74274 Nov  7  2019  crutches.svg
-rw-r--r--   1 sticks sticks      13420 Jun 24  2019  Cry_Kathy.png
drwx------   2 sticks sticks       4096 Feb 15  2023  .cups
drwx------   2 sticks sticks       4096 Aug 31 04:15  data
drwx------   2 sticks sticks       4096 Aug 31 04:15  datapacks
drwx------   2 sticks sticks       4096 Aug 31 04:15  db
drwx------   3 sticks sticks       4096 Oct 19  2017  .dbus
drwx------   2 sticks sticks       4096 Aug 31 04:15  ddgr
-rw-rw-r--   1 sticks sticks        519 Jun 24  2019  dead_classmates.txt
-rw-------   1 sticks sticks        148 Jun 24  2019  dead.letter
drwx------   2 sticks sticks       4096 Aug 31 04:15  death_star_data
-rw-r--r--   1 sticks sticks      53486 Aug 28  2020  debate.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  debian-installation
-rw-r--r--   1 sticks sticks        984 Jun 24  2019  default.gpfl
-rw-r--r--   1 sticks sticks      44104 Jun 10  2020  defund_Congress.jpg
-rw-r--r--   1 sticks sticks      75810 Jun 10  2020  defund_Congress.png
-rw-r--r--   1 sticks sticks       5530 Jun 10  2020  defund_Congress.svg
-rw-------   1 sticks sticks        136 Jun 24  2019  derby.log
drwxrwxrwx   3 sticks sticks       4096 Mar 24  2023  .designer
drwx------   2 sticks sticks       4096 Aug 31 04:15  Desktop
drwx------   2 sticks sticks       4096 Aug 31 04:15  deviantart
-rw-rw-r--   1 sticks sticks   70119594 Oct 31  2022  DHD-Ep-037-Final-Edit.ogg
lrwxrwxrwx   1 sticks sticks         16 Jan  3  2020  DI -> /mnt/diskImages/
-rw-------   1 sticks sticks        467 Jan 10  2017  digital_ocean_sticks_keys.tgz
drwx------   2 sticks sticks       4096 Aug 31 04:15  DIM-1
drwx------   2 sticks sticks       4096 Aug 31 04:15  DIM1
-rw-rw-r--   1 sticks sticks       3494 Jul 19  2021  .dircolors
-rw-------   1 sticks sticks        149 Jun 24  2019  .directory
drwx------   2 sticks sticks       4096 Jan  3  2014  .distlib
drwx------   2 sticks sticks       4096 Aug 31 04:15  DJ-Mason
drwx------   2 sticks sticks       4096 Aug 31 04:15  dkrproject
drwx------   2 sticks sticks       4096 Aug 31 04:15  dkrVol
drwx------   2 sticks sticks       4096 Aug 31 04:15  dmca
-rw-r--r--   1 sticks sticks         23 Apr 26  2020  .dmrc
drwx------   2 sticks sticks       4096 Aug 31 04:15  DO
drwx------  11 sticks sticks       4096 Aug 13 10:38  .docker
drwx------   2 sticks sticks       4096 Aug 31 04:15  docker
-rw-rw-r--   1 sticks sticks       2760 Aug 27  2021  docker-keyring.gpg
drwx------  44 sticks sticks      24576 Sep 30 19:31  Documents
drwx------   2 sticks sticks       4096 Aug 31 04:15  DO_Logo_Assets
-rw-r--r--   1 sticks sticks        286 Jun 17  2020  domains.pt
drwx------   2 sticks sticks       4096 Aug 31 04:15  DoMcSvr
drwxrwxr-x  12 sticks sticks       4096 Sep 22 03:10  .dotfiles
drwx------   2 sticks sticks       4096 Aug 31 04:15  dotfilesgit
drwx------   2 sticks sticks       4096 Oct  8 22:19  Downloads
-rw-r--r--   1 sticks sticks      56379 Jun 28  2020  drawing-1.svg
-rw-r--r--   1 sticks sticks     554213 Jul 17  2020  dreaming_sleep.png
-rw-r--r--   1 sticks sticks       3149 May  4  2015  .dreampie
-rw-rw-r--   1 sticks sticks    4450297 Dec  8  2024  Drivers_Licence.zip
drwx------   2 sticks sticks       4096 Aug 31 04:15  drkVol
drwx------   8 sticks sticks       4096 Feb 15  2023  .dropbox
drwx------   2 sticks sticks       4096 Aug 31 04:15  Dropbox
drwxrwxr-x   3 sticks sticks       4096 Jul 20  2020  .dropbox-dist
drwx------   2 sticks sticks       4096 Aug 31 04:15 'Dropbox (Old)'
drwx------ 208 sticks sticks      20480 Jan 12  2025  .dvdcss
drwx------   2 sticks sticks       4096 Aug 31 04:15  .dvdrip
-rw-r--r--   1 sticks sticks      29142 Jun 24  2019  .dvdriprc
drwx------   2 sticks sticks       4096 Aug 31 04:15  dwhelper
-rwxrwxr-x   1 sticks sticks         93 Jun 24  2019  dwtd.sh
-rw-r--r--   1 sticks sticks      30298 Sep 12  2020  EB-09-11-20.txt
-rw-r--r--   1 sticks sticks       7777 Nov  1  2019  eb_build1
drwx------   2 sticks sticks       4096 Aug 31 04:15  .eBook-speaker
-rw-r--r--   1 sticks sticks    1120666 Apr 13  2020  EB-Silent-Zeb_13_09-34-40.png
-rw-r--r--   1 sticks sticks       2829 Oct 31  2019  eb_sucks.svg.svg
drwx------   2 sticks sticks       4096 Aug 31 04:15  .electron
drwx------   2 sticks sticks       4096 Aug 31 04:15  .electron-gyp
drwx------   2 sticks sticks       4096 Aug 31 04:15  .elinks
-rw-rw-r--   1 sticks sticks        447 Jun 13  2024  Ely.csv
drwx------   2 sticks sticks       4096 Aug 31 04:15  .emacs.d
-rw-r--r--   1 sticks sticks     849153 Jun 24  2019  Embarrass_Maxine.png
-rw-rw-rw-   1 sticks sticks        170 Jun 14  2023  Endeavouros_Cassini_Nova-03-2023_R2.iso.sha512sum
drwx------   2 sticks sticks       4096 Aug 31 04:15  .entagged
drwx------   2 sticks sticks       4096 Aug 31 04:15  environments
drwx------   2 sticks sticks       4096 Aug 31 04:15  .eric4
-rw-------   1 sticks sticks         16 Jun 24  2019  .esd_auth
drwx------   2 sticks sticks       4096 Aug 31 04:15  espeak-data
-rw-r--r--   1 sticks sticks        451 Feb 24  2022  .espeakedit
drwx------   2 sticks sticks       4096 Aug 31 04:15  .etracer
-rw-rw-r--   1 sticks sticks         45 Jun  3  2018  ETS2_Profiles.tar.gz
drwx------   2 sticks sticks       4096 Aug 31 04:15  .everpad
-rw-rw-r--   1 sticks sticks     241307 Jul 19  2022  example.json
-rw-r--r--   1 sticks sticks       8980 Sep 15  2020  examples.desktop
drwx------   2 sticks sticks       4096 Aug 31 04:15  exercises
-rwxr-xr-x   1 sticks sticks    4690368 Feb  9  2023  external-editor-revived
drwx------   2 sticks sticks       4096 Aug 31 04:15  eXtremeGammon
-rw-r--r--   1 sticks sticks      42886 Jun 24  2019  F1-F4.jpg
lrwxrwxrwx   1 sticks sticks         42 May  9  2020  f2c -> /home/sticks/src/pythonfiles/fahren2cel.py
-rw-r--r--   1 sticks sticks      46886 Jan  7  2018  F5-F8.jpg
-rw-r--r--   1 sticks sticks      58626 Jun 24  2019  F9-F12.jpg
-rw-r--r--   1 sticks sticks       1663 Apr 26  2020  .face
-rw-rw-r--   1 sticks sticks        186 Oct  8 01:26  factor.lua
drwx------   2 sticks sticks       4096 Aug 31 04:15  .fbmessenger
-rw-rw-r--   1 sticks sticks     611174 Jan  6  2024  feh_066475_000001_Santa_Rugged.png
-rw-rw-r--   1 sticks sticks      13175 Aug 14  2023  feh_152907_000001_ubuntu-logo-icon.png
-rwxr-xr--   1 sticks sticks        120 Sep 15  2020  .fehbg
-rw-r--r--   1 sticks sticks       1055 Jun 24  2019  .festival_history
-rw-r--r--   1 sticks sticks        104 Jun 24  2019  file1.txt
-rw-r--r--   1 sticks sticks        401 Jun 17  2020  file2
-rw-rw-r--   1 sticks sticks      20828 Jun 24  2019  filename.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .filezilla
-rwxr-xr-x   1 sticks sticks      10240 Feb 27  2023  findit
-rw-r--r--   1 sticks sticks       2234 Feb 27  2023  findithelp.txt
-rw-rw-r--   1 sticks sticks   22014404 Jun  4  2023  FiraCode.zip
-rwxrwxr-x   1 sticks sticks        698 Sep 24 15:31  fix_keyring.sh
-rw-rw-r--   1 sticks sticks      10059 Apr  1  2025  flatlist
drwx------   2 sticks sticks       4096 Aug 31 04:15  .fltk
-rw-r--r--   1 sticks sticks          5 Jun 24  2019  .fluxgui.pid
-rw-rw-r--   1 sticks sticks         43 Aug 28  2022  fn
drwx------   2 sticks sticks       4096 Aug 31 04:15  .fontconfig
drwxrwxr-x   5 sticks sticks       4096 Dec  5  2020  .Fontmatrix
drwx------   2 sticks sticks       4096 Aug 31 04:15  .fonts
-rw-rw-r--   1 sticks sticks    1522851 Mar 14  2022  forge-1.18.2-40.0.15-installer.jar.log
-rw-rw-r--   1 sticks sticks     704548 Sep 24  2022  forge-1.18.2-40.0.44-installer.jar.log
drwx------   2 sticks sticks       4096 Aug 31 04:15  free-programming-books-master
drwx------   2 sticks sticks       4096 Aug 31 04:15  .freerdp
drwx------   2 sticks sticks       4096 Aug 31 04:15  .furiusisomount
drwxrwxr-x  11 sticks sticks       4096 Oct  2 01:14  .fzf
-rw-rw-r--   1 sticks sticks        149 Oct  2 01:28  .fzf.bash
-rwxrwxr-x   1 sticks sticks        530 Sep 21 20:56  fzf_fix.sh
-rw-rw-r--   1 sticks sticks        417 Oct  2 01:33  .fzf.zsh
-rw-rw-r--   1 sticks sticks        148 Oct  2 00:32  .fzf.zsh.backup
drwx------   2 sticks sticks       4096 Aug 31 04:15  Games
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gconf
-rw-------   1 sticks sticks        334 Jun 24  2019  gcp.conf
lrwxrwxrwx   1 sticks sticks         55 Jul 31  2020  gd -> '/home/sticks/Insync/gimpysticks@gmail.com/Google Drive/'
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gdesklets
-rw-r--r--   1 sticks sticks      28747 Jun 24  2019  geckodriver.log
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gEcrit
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gegl-0.0
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gem
drwx------   3 sticks sticks       4096 Oct  2 00:56  .gemini
-rw-r--r--   1 sticks sticks   34101257 Mar 22  2023 'General_Beta_VMS Lite_Win32_V1.0.3.6.T.20230315.exe'
drwx------   3 sticks sticks       4096 Apr 17  2015  .Genymobile
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gespeaker
-rw-rw-r--   1 sticks sticks      20554 Aug  7 07:56  get-docker.sh
-rw-r--r--   1 sticks sticks    1775835 Nov 23  2019  get-pip.py
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gimp-2.6
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gimp-2.6-backup
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gimp-2.8
drwx------   2 sticks sticks       4096 Aug 31 04:15  gimpy.t.o.c.f_home
-rw-rw-r--   1 sticks sticks     179975 Mar  7  2018  git2ndedit.txt
-rw-r--r--   1 sticks sticks        645 Dec 16  2019  gitbooks
lrwxrwxrwx   1 sticks sticks         24 Dec 17  2021  .gitconfig -> .dotfiles/git/.gitconfig
-rw-------   1 sticks sticks        230 Oct  9 01:18  .git-credentials
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gitkraken
drwx------   2 sticks sticks       4096 Aug 31 04:15  .git-templates
-rw-rw-r--   1 sticks sticks  290679871 Jun 24  2019 'Git Tutorial for Beginners - A Quick Start Guide-ugN-IYV1NTM.mkv'
-rw-rw-r--   1 sticks sticks  290679871 Jun 24  2019  Git_Tutorial_for_Beginners-A_Quick_Start_Guide-ugN-IYV1NTM.mkv
-rw-r--r--   1 sticks sticks       3884 Sep 12  2020  .gmrun_history
-rw-r--r--   1 sticks sticks       1465 Sep  8  2020  .gmrunrc
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gnome
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gnome2
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gnome2_private
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gnubg
drwx------   2 sticks sticks       4096 Aug 31 04:15  gnubg-sound
-rw-rw-r--   1 sticks sticks     733327 Nov 19  2020  gnubg-sounds-1.06.002-37.17.x86_64.rpm
-rw-rw-r--   1 sticks sticks      28828 Jan 26  2021  gnubg-sticks_7p_2021-01-26.sgf
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gnucash
drwx------   2 sticks sticks       4096 Oct  3 15:42  .gnupg
drwx------   2 sticks sticks       4096 Aug 31 04:15  GNUstep
drwx------   2 sticks sticks       4096 Aug 31 04:15  go
drwx------   2 sticks sticks       4096 Aug 31 04:15  .google
-rw-rw-r--   1 sticks sticks   51690924 Jun 24  2019  google-chrome-stable_current_amd64.deb.1
drwx------   2 sticks sticks       4096 Aug 31 04:15  .googleearth
-rw-r--r--   1 sticks sticks        377 Jun 24  2019  google_home_Christmas.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  google-python-exercises
drwx------   2 sticks sticks       4096 Aug 31 04:15  google_takeout
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gphoto
drwx------   2 sticks sticks       4096 Aug 31 04:15  gPodder
drwx------   2 sticks sticks       4096 Aug 31 04:15  GPUCache
drwx------   2 sticks sticks       4096 Aug 31 04:15  .grip
drwx------   2 sticks sticks       4096 Aug 31 04:15  .grok
drwx------   2 sticks sticks       4096 Aug 31 04:15  .grsync
drwx------   2 sticks sticks       4096 Aug 31 04:15  .gstreamer-0.10
-rw-r--r--   1 sticks sticks        108 Jun 24  2019  .gtk-bookmarks
-rw-r--r--   1 sticks sticks        547 Apr 26  2020  .gtkrc-2.0
-rw-r--r--   1 sticks sticks         97 Jul 30  2020  guess.py
drwx------   2 sticks sticks       4096 Aug 31 04:15  .hardinfo
-rw-r--r--   1 sticks sticks      29181 Aug  7  2017  hbhelp.txt
-rw-r--r--   1 sticks sticks    2179555 Jun 12  2016  headshot.xcf
-rw-rw-r--   1 sticks sticks        566 Dec 27  2020  help
-rw-rw-r--   1 sticks sticks        804 Apr 26  2023  Help_Services.csv
-rw-rw-r--   1 sticks sticks       2078 Jul 19  2021  help.txt
-rw-rw-r--   1 sticks sticks       2576 Oct  9  2020  help.yml
-rw-rw-r--   1 sticks sticks       3595 Sep 29  2023  Herman_Kerry.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  HG
-rw-rw-r--   1 sticks sticks        633 Dec  5  2020  HG_list.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  history
-rw-rw-r--   1 sticks sticks     485440 Feb 26  2023 'How to reset Google Nest Mini - #Shorts [CcTBldZp2xE].opus'
-rw-r-----   1 sticks sticks      14987 Jun 24  2019  hp-check.log
drwx------   2 sticks sticks       4096 Aug 31 04:15  .hplip
-rw-r--r--   1 sticks sticks   20138067 Jun 24  2019  hpr2794.ogg
-rw-r--r--   1 sticks sticks        573 Jun 24  2019  hs_err_pid10339.log
-rw-r--r--   1 sticks sticks      68438 Jun 24  2019  hs_err_pid8670.log
-rw-r--r--   1 sticks sticks     116641 Mar 31  2017  hs_err_pid9066.log
-rw-r--r--   1 sticks sticks        522 Jun 24  2019  .huludesktop
drwx------   2 sticks sticks       4096 Aug 31 04:15  .hydrogen
drwx------   2 sticks sticks       4096 Aug 31 04:15  .hypnotix
-rw-r--r--   1 sticks sticks      66890 Dec  4  2019  i3config.ps
-rw-------   1 sticks sticks     239446 Jun 24  2019  .ICEauthority
drwx------   2 sticks sticks       4096 Aug 31 04:15  .icon
-rw-r--r--   1 sticks sticks       5816 Sep 28  2020  icon.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  .icons
drwx------   2 sticks sticks       4096 Aug 31 04:15  icons
drwx------   2 sticks sticks       4096 Aug 31 04:15  .idea
drwx------   4 sticks sticks       4096 Feb 17  2015  .IdeaIC14
drwx------   4 sticks sticks       4096 Feb  7  2017  .IdeaIC2016.3
drwx------   2 sticks sticks       4096 Aug 31 04:15  IdeaProjects
drwx------   2 sticks sticks       4096 Aug 31 04:15  .idlerc
-rw-r--r--   1 sticks sticks      99887 May 25  2020  IG-Test.png
-rw-r--r--   1 sticks sticks      11604 Jun 24  2019  .ilg-config
-rw-r--r--   1 sticks sticks        621 Jun 24  2019  il-links.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  images
-rwxr-xr-x   1 sticks sticks        155 Jun 24  2019  imandl.sh
-rw-r--r--   1 sticks sticks    4565546 Jun 24  2019  IMG_20170624_115652.jpg
-rw-r--r--   1 sticks sticks        345 Jun 24  2019  .imwheelrc
-rw-rw-r--   1 sticks sticks       5011 Jun 24  2019  index.html
drwx------   2 sticks sticks       4096 Aug 31 04:15  .indicator-weather
-rw-r--r--   1 sticks sticks       3797 Sep  6  2016  Inkscape_Test.svg
drwx------   2 sticks sticks       4096 Aug 31 04:15  inkscape_tutorial
-rw-rw-r--   1 sticks sticks         65 Nov  2  2021  .inputrc
drwx------   2 sticks sticks       4096 Aug 31 04:15  Inspection
-rw-r--r--   1 sticks sticks         42 Jun 24  2019  .install4j
-rw-r--r--   1 sticks sticks       5673 Jan  3  2020  install.err
drwx------   2 sticks sticks       4096 Aug 31 04:15  install-gnome-themes
-rw-rw-r--   1 sticks sticks        838 May 17  2021  install_haxk.zip
-rw-rw-r--   1 sticks sticks      19511 Sep 21 22:11  install.sh
-rwxrwxr-x   1 sticks sticks        246 Jun 24  2019  instmc.sh
drwx------   2 sticks sticks       4096 Aug 31 04:15  interfaceLift_Wallpapers
drwx------   2 sticks sticks       4096 Aug 31 04:15  Introduction-Programming-Python-master
drwx------   2 sticks sticks       4096 Aug 31 04:15  .ipynb_checkpoints
drwx------   2 sticks sticks       4096 Aug 31 04:15  .ipython
drwx------   2 sticks sticks       4096 Aug 31 04:15  .irssi
-rwxrwxr-x   1 sticks sticks        105 Jun 24  2019  ismnt.sh
drwx------   2 sticks sticks       4096 Aug 31 04:15  .java
-rw-rw-r--   1 sticks sticks       8192 Jun 24  2019  java.txt
-rw-r--r--   1 sticks sticks        972 Jun 24  2019  jaytech.m3u
-rw-r--r--   1 sticks sticks         66 Jun 24  2019  jblive.m3u
-rw-------   1 sticks sticks       1320 Mar 26  2015  jcameron-key.asc
-rw-rw-r--   1 sticks sticks       1320 Jun 24  2019  jcameron-key.asc.1
drwx------   2 sticks sticks       4096 Aug 31 04:15  .jedit
-rw-r--r--   1 sticks sticks       7226 Jun 24  2019  Jenkees.m3u
drwx------   2 sticks sticks       4096 Aug 31 04:15  .jftp
-rw-rw-r--   1 sticks sticks     149777 Aug  7  2021  Jj.png
-rw-r--r--   1 sticks sticks       1109 Jun 24  2019  jkdesktop_ifconfig.txt
-rw-------   1 sticks sticks       2493 Apr 28  2021 'John Kilbane.asc'
-rw-------   1 sticks sticks       1780 Nov 15  2020 'John Kilbane.pgp'
-rw-r--r--   1 sticks sticks   74150162 Oct 28  2018  Julian_Winding-The_Demon_Dance-From_THE_NEON_DEMON_OS.flac
drwx------   2 sticks sticks       4096 Aug 31 04:15  .juniper_networks
drwx------   2 sticks sticks       4096 Aug 31 04:15  .jupyter
drwx------   2 sticks sticks       4096 Aug 31 04:15  .kchmviewer
drwx------   2 sticks sticks       4096 Aug 31 04:15  .kde
drwx------   2 sticks sticks       4096 Aug 31 04:15  kdenlive
-rw-rw-rw-   1 sticks sticks     451550 Jun 16  2023  keybindings_backup.ini
-rw-rw-r--   1 sticks sticks       7436 Jul  2  2023  keybindings.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .kiki
drwx------   2 sticks sticks       4096 Aug 31 04:15  Kilbane_Statements
drwx------   2 sticks sticks       4096 Aug 31 04:15  .kingsoft
drwx------   2 sticks sticks       4096 Aug 31 04:15  .kismet
-rw-r--r--   1 sticks sticks        264 Jun 24  2019  Kismet-20160220-14-13-56-1.gpsxml
-rw-r--r--   1 sticks sticks        103 Jun 24  2019  Kismet-20160220-14-13-56-1.nettxt
-rw-r--r--   1 sticks sticks        222 Jun 24  2019  Kismet-20160220-14-13-56-1.netxml
-rw-r--r--   1 sticks sticks         24 Jun 24  2019  Kismet-20160220-14-13-56-1.pcapdump
drwx------   2 sticks sticks       4096 Aug 31 04:15  .kivy
drwx------   2 sticks sticks       4096 Aug 31 04:15  .kodi
-rw-r--r--   1 sticks sticks      37041 Jun 24  2019  kodi_crashlog-20170626_235919.log
drwx------   2 sticks sticks       4096 Aug 31 04:15  konsolethemes
-rw-rw-r--   1 sticks sticks         19 Jun 24  2019  kwinfix.txt
-rw-rw-r--   1 sticks sticks      18370 Jun 24  2019  lastnames.xlsm
drwx------   2 sticks sticks       4096 Aug 31 04:15  .launchpadlib
drwx------   2 sticks sticks       4096 Aug 31 04:15  lb
-rw-r--r--   1 sticks sticks     112974 Apr 13  2020  Leekes_at_BCSD.jpg
drwx------   2 sticks sticks       4096 Aug 31 04:15  .lein
-rw-------   1 sticks sticks        681 Oct  8 23:04  .lesshst
drwx------   2 sticks sticks       4096 Aug 31 04:15  .lgames
drwxrwxr-x   3 sticks sticks       4096 Sep 22 02:40  lib
drwx------   2 sticks sticks       4096 Aug 31 04:15  libbluray
-rw-r--r--   1 sticks sticks        175 Jun 24  2019  libdvd_pkg.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  libraries
drwx------   2 sticks sticks       4096 Aug 31 04:15  .librewolf
-rw-r--r--   1 sticks sticks       1071 Sep 17 14:41  LICENSE
drwx------   2 sticks sticks       4096 Aug 31 04:15  .links2
drwx------   2 sticks sticks       4096 Aug 31 04:15  linux32
drwx------   2 sticks sticks       4096 Aug 31 04:15  linux64
drwx------   2 sticks sticks       4096 Aug 31 04:15  linuxjournal
drwx------   2 sticks sticks       4096 Aug 31 04:15  .linuxmint
drwx------   2 sticks sticks       4096 Aug 31 04:15  .lispeak
-rw-rw-r--   1 sticks sticks    1870492 Aug 29  2022  listfilesrepo.tgz
-rw-r--r--   1 sticks sticks      10956 Jun 24  2019  lists
-rw-rw-r--   1 sticks sticks 2782080790 Jan 30  2025 'LIVE： Kash Patel’s confirmation hearing for FBI director [0YPoHEUlFNw].webm'
dr-x------   2 sticks sticks       4096 Aug 31 04:15  LJArchive1994-2018
drwx------   2 sticks sticks       4096 Aug 31 04:15  lmms
-rw-r--r--   1 sticks sticks       4804 Apr 30  2022  .lmmsrc.xml
-rwxrwxr-x   1 sticks sticks       3563 Jun 24  2019  loadicons.sh
drwx------   6 sticks sticks       4096 Sep 22 02:40  .local
-rwxrwxr-x   1 sticks sticks        315 Aug  2 21:00  LocationEd.desktop
drwx------   2 sticks sticks       4096 Aug 31 04:15  .log
drwx------   2 sticks sticks       4096 Aug 31 04:15  logs
-rw-rw-r--   1 sticks sticks       3946 Apr 17  2022  Lorem2.txt
-rw-r--r--   1 sticks sticks       3946 Mar 19  2020  lorem.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  lpthw
-rw-rw-r--   1 sticks sticks      24800 Jun 24  2019  lshw.pdf
-rw-r--r--   1 sticks sticks       1839 Jun 24  2019  .luc
drwx------   2 sticks sticks       4096 Aug 31 04:15  .luckyBackup
drwx------   2 sticks sticks       4096 Aug 31 04:15  .luckybackup-snaphots
drwx------   2 sticks sticks       4096 Aug 31 04:15  .lwsm
-rw-rw-r--   1 sticks sticks    1340634 Apr  7  2022  lynx.cfg
drwx------   2 sticks sticks       4096 Aug 31 04:15  .m2
drwx------   2 sticks sticks       4096 Aug 31 04:15  .macromedia
drwx------   2 sticks sticks       4096 Aug 31 04:15  makedeb
drwxr-xr-x   2 sticks sticks       4096 Oct  2  2020  .MakeMKV
drwx------   2 sticks sticks       4096 Aug 31 04:15  .mame
drwx------   2 sticks sticks       4096 Aug 31 04:15  mame
-rw-rw-r--   1 sticks sticks        634 Mar  4  2024  mangrove
-rw-r--r--   1 sticks sticks       1340 Aug 20  2020  markdown_practice.md
drwx------   2 sticks sticks       4096 Aug 31 04:15  mark_read
-rwxrwxr-x   1 sticks sticks        151 Jul 23  2023  mase
drwx------   2 sticks sticks       4096 Aug 31 04:15  MasonAudio
-rw-r--r--   1 sticks sticks     682768 Jun 24  2019  Mason_Florence_Freedom.JPG
-rw-r--r--   1 sticks sticks       5803 Apr 12  2020  masonfwalls@192.168.0.130
drwx------   2 sticks sticks       4096 Aug 31 04:15  masonkidspc
drwx------   2 sticks sticks       4096 Aug 31 04:15  mason_mc
drwx------   2 sticks sticks       4096 Aug 31 04:15  mason_videos
drwx------   2 sticks sticks       4096 Aug 31 04:15  .masterpdfeditor
-rw-rw-r--   1 sticks sticks      24226 Feb  7  2021  matrix_invite.png
-rw-r--r--   1 sticks sticks       6910 Jun 24  2019  matrix_riot_link.png
-rw-r--r--   1 sticks sticks          2 Nov  1  2019  .mbsyncrc
-rw-r--r--   1 sticks sticks         61 Jun 19  2020  MC_Coords.txt
-rw-rw-r--   1 sticks sticks      58498 Sep 18  2020  mcfiles
drwx------   2 sticks sticks       4096 Aug 31 04:15  MC_Music
drwx------   2 sticks sticks       4096 Aug 31 04:15  mc_server
drwxr-xr-x   2 sticks sticks       4096 Feb 12  2020  .MCTranscodingSDK
-rw-rw-r--   1 sticks sticks       3570 Oct  6  2023  md_preview_config
-rw-rw-r--   1 sticks sticks     141419 May  4  2018  Metamorphosis.txt
lrwxrwxrwx   1 sticks sticks         32 Jan  6  2024  Midjourney -> /home/sticks/Pictures/Midjourney
-rw-r--r--   1 sticks sticks         39 Jun 24  2019  .mime.types
drwx------   2 sticks sticks       4096 Aug 31 04:15  mimic3_docker_Deb_build
lrwxrwxrwx   1 sticks sticks         57 Nov 21  2021  .minecraft -> /home/sticks/.var/app/com.mojang.Minecraft/data/minecraft
drwx------   2 sticks sticks       4096 Aug 31 04:15  .mission-control
-rw-rw-r--   1 sticks sticks      13725 Jun  9  2024  mntadult.files
drwx------   2 sticks sticks       4096 Aug 31 04:15  mods
drwx------   2 sticks sticks       4096 Aug 31 04:15  Moms_Pics
drwx------   2 sticks sticks       4096 Aug 31 04:15  .mono
drwx------   2 sticks sticks       4096 Aug 31 04:15  .motion
drwx------   5 sticks sticks       4096 Sep 21 23:15  .mozilla
-rw-r--r--   1 sticks sticks     207038 Apr 20  2020  mp3list
-rw-rw-r--   1 sticks sticks       4455 Jul 21  2023  mp4list
drwx------   2 sticks sticks       4096 Aug 31 04:15  .mplayer
-rw-rw-r--   1 sticks sticks      43167 Jan 20  2024  mpv-shot0001.jpg
-rw-rw-r--   1 sticks sticks      45426 Jan 20  2024  mpv-shot0002.jpg
-rw-rw-r--   1 sticks sticks      53327 Jan 20  2024  mpv-shot0003.jpg
-rw-rw-r--   1 sticks sticks      39400 Jan 20  2024  mpv-shot0004.jpg
-rw-rw-r--   1 sticks sticks      39802 Jan 20  2024  mpv-shot0005.jpg
-rw-rw-r--   1 sticks sticks      41507 Jan 20  2024  mpv-shot0006.jpg
-rw-rw-r--   1 sticks sticks      10203 Jun 19  2023  msbubbles
-rw-rw-r--   1 sticks sticks        191 Jun 24  2019  msg
-rw-r--r--   1 sticks sticks        210 Jun 24  2019  msgtest.sh
-rw-r--r--   1 sticks sticks        825 Oct 23  2019  multiurls
drwx------   4 sticks sticks       4096 Oct  5 23:58  Music
-rwxr-xr-x   1 sticks sticks       1538 Jun 24  2019  mvbg
-rwxrwxr-x   1 sticks sticks       6427 Mar  7  2021  mv_movies.sh
-rw-r--r--   1 sticks sticks         73 Mar  7  2021  mv_Movies.tmp
-rw-rw-rw-   1 sticks sticks       2050 May 19  2023  mvpl
-rw-rw-r--   1 sticks sticks    7693593 Jun 17  2022  mwalls4464@192.168.0.130
drwx------   2 sticks sticks       4096 Aug 31 04:15  My_Barnes_and_Noble_eBooks
drwx------   2 sticks sticks       4096 Aug 31 04:15 'My Barnes & Noble eBooks'
drwx------   2 sticks sticks       4096 Aug 31 04:15 'My Digital Editions'
drwx------   2 sticks sticks       4096 Aug 31 04:15  My_Digital_Editions
-rw-rw-r--   1 sticks sticks          0 Mar 27  2025  myfile.txt
-rw-rw-r--   1 sticks sticks      17221 May  1 03:22  myinstalls.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .mypaint
-rw-rw-r--   1 sticks sticks      41971 Jun 24  2019  my_photo.jpg
-rw-rw-r--   1 sticks sticks     372100 Feb 19  2025  mysettings.conf
drwx------   2 sticks sticks       4096 Aug 31 04:15  .mysql
-rw-------   1 sticks sticks          5 Jun 24  2019  .mysql_history
-rw-rw-rw-   1 sticks sticks      68430 Mar  5  2023  my_video-1.mkv
-rw-rw-rw-   1 sticks sticks    8638661 Mar 16  2023  my_video-2.mkv
-rw-rw-rw-   1 sticks sticks    7494182 Mar 16  2023  my_video-3.mkv
drwx------   2 sticks sticks       4096 Aug 31 04:15  .nano
-rw-r--r--   1 sticks sticks       2651 Apr  5  2019  .nanorc
drwx------   2 sticks sticks       4096 Aug 31 04:15  nashome
drwx------   2 sticks sticks       4096 Aug 31 04:15  nas_sticks
-rw-rw-rw-   1 sticks sticks        616 Oct 15  2022  nazi_playlist
drwx------   2 sticks sticks       4096 Aug 31 04:15  .ne
-rw-r--r--   1 sticks sticks     445123 Dec 29  2019  neof.gif
drwx------   2 sticks sticks       4096 Aug 31 04:15  nerd-dictation
-rw-rw-r--   1 sticks sticks         92 Mar  5  2025  nerd-dictation.log
drwx------   2 sticks sticks       4096 Aug 31 04:15  nerd-fonts
drwx------   2 sticks sticks       4096 Aug 31 04:15  .nevernote
-rw-rw-r--   1 sticks sticks         99 Jun 24  2019  newalias
-rw-r--r--   1 sticks sticks       3062 Oct 31  2019 'New document 1.2019_10_31_01_27_58.0.svg'
-rw-r--r--   1 sticks sticks       9422 Aug 26  2020 'New document 1.2020_08_26_11_22_07.0.svg'
-rw-r--r--   1 sticks sticks      11644 Aug 27  2020 'New document 1.2020_08_27_21_13_31.0.svg'
drwx------   2 sticks sticks       4096 Aug 31 04:15  New_Fonts
drwx------   2 sticks sticks       4096 Aug 31 04:15  .newsboat
-rw-r--r--   1 sticks sticks       3909 Jun 24  2019  new_vimhis
drwx------   2 sticks sticks       4096 Aug 31 04:15  nick_mc
-rw-rw-rw-   1 sticks sticks     302068 Jun 23  2023  Nick_Schedule_06-23.jpeg
-rw-rw-rw-   1 sticks sticks     302068 Jun 23  2023  Nicks_Sched_06.jpeg
drwx------   2 sticks sticks       4096 Aug 31 04:15  nickwalls
drwx------   2 sticks sticks       4096 Aug 31 04:15  .nightingale
-rw-r--r--   1 sticks sticks   88059985 Oct 22  2019  NIGHT_of_the_LIVING_SNOWFLAKE-MOZA3Oo7BU0.mkv
drwx------   2 sticks sticks       4096 Aug 31 04:15  .ninja_ide
-rw-r--r--   1 sticks sticks       4338 Jun 24  2019  Nixie1.osp
-rw-r--r--   1 sticks sticks      40092 Jun 24  2019  nmap.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .node-gyp
drwx------   2 sticks sticks       4096 Aug 31 04:15  node_modules
-rw-------   1 sticks sticks         76 Jul 20  2023  .node_repl_history
drwx------   2 sticks sticks       4096 Aug 31 04:15  node-v18.12.1-linux-x64
-rw-rw-r--   1 sticks sticks       5048 Feb  9  2024  nordinst
drwx------   2 sticks sticks       4096 Aug 31 04:15  nord_ovpn
drwx------   2 sticks sticks       4096 Aug 31 04:15  .notifications
-rw-r--r--   1 sticks sticks       5587 Nov 20  2019  notifyd.log
-rwxr-xr-x   1 sticks sticks        201 Jun 24  2019  notify-myself.sh
-rw-rw-r--   1 sticks sticks        605 Mar 13  2018  .notify-osd
drwx------   2 sticks sticks       4096 Aug 31 04:15  .notifyosdconf
-rw-r--r--   1 sticks sticks        232 Jun 24  2019  .notmuch-config
drwx------   4 sticks sticks       4096 Aug 31 04:15  .npm
-rw-------   1 sticks sticks         12 Mar 25  2020  .npmrc
-rw-rw-r--   1 sticks sticks      61593 Feb  7  2021  n_telegram_invite.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  .nv
-rw-r--r--   1 sticks sticks        470 Sep 27 00:26  .nvidia-settings-rc
drwx------   2 sticks sticks       4096 Aug 31 04:15  nvim
drwx------   2 sticks sticks       4096 Aug 31 04:15  nvim.backup
drwx------   8 sticks sticks       4096 Aug 31 04:15  .nvm
drwx------   2 sticks sticks       4096 Aug 31 04:15  .nylas
-rw-r--r--   1 sticks sticks       4112 Jan 18  2019  OB_Keybindings.txt
-rw-r--r--   1 sticks sticks        121 Jun 24  2019  .odbc.ini
drwx------   2 sticks sticks       4096 Aug 31 04:15  .odin
-rw-r--r--   1 sticks sticks     116228 Jun 24  2019  offseason.jpg
-rw-r--r--   1 sticks sticks      26786 Jul 11  2020  oggslist
drwxr-xr-x  13 sticks sticks       4096 Oct  4 22:16  .oh-my-zsh
drwx------   2 sticks sticks       4096 Aug 31 04:15 'Old Firefox Data'
-rw-rw-r--   1 sticks sticks       1321 Jun  8  2024  omz_history
drwx------   2 sticks sticks       4096 Aug 31 04:15  onedark.vim
drwx------   2 sticks sticks       4096 Aug 31 04:15  online-learning-resources
-rw-------   1 sticks sticks      51401 Feb 16  2021 'Online Return Center.pdf'
drwx------   2 sticks sticks       4096 Aug 31 04:15  OpenAudible
drwx------   2 sticks sticks       4096 Aug 31 04:15  .openshot
drwx------   2 sticks sticks       4096 Aug 31 04:15  .openshot_qt
-rw-r--r--   1 sticks sticks       2799 Oct  9  2020  options.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .oracle_jre_usage
-rw-rw-rw-   1 sticks sticks     210025 Oct 10  2022 'Order Confirmation - Blair Tech.pdf'
-rw-rw-r--   1 sticks sticks       4311 Apr  1  2025  orphans
-rw-r--r--   1 sticks sticks       3453 Nov  1  2019  outlined_Font.svg
-rw-rw-r--   1 sticks sticks       2137 Feb  9  2024  output
-rw-rw-r--   1 sticks sticks   17280467 Sep  5  2021  output1.mkv
-rw-rw-r--   1 sticks sticks      86127 Aug  1 01:20  output.md
-rw-r--r--   1 sticks sticks          7 Nov 14  2019  .overgrive.lock
-rw-r--r--   1 sticks sticks   12908437 Nov 14  2019  .overgrive.log
-rw-r--r--   1 sticks sticks   23186847 Oct 24  2019  .overgrive.log.old
-rw-r--r--   1 sticks sticks   25571571 Sep 24  2021  ovpn.zip
drwx------   2 sticks sticks       4096 Aug 31 04:15  package
-rw-rw-rw-   1 sticks sticks        149 Apr  3  2025  package.json
-rw-rw-rw-   1 sticks sticks      20334 Apr  3  2025  package-lock.json
-rw-r--r--   1 sticks sticks        361 Sep 15  2020  .pam_environment
-rw-r--r--   1 sticks sticks     336501 Oct 20  2019  Panera.png
-rw-r--r--   1 sticks sticks       6540 Jun 24  2019  papaw.gnucash.20160619181053.gnucash
-rw-rw-r--   1 sticks sticks       3764 Feb 19  2024  papaw_Keyboard.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .parallel
-rw-rw-rw-   1 sticks sticks      11350 Dec 26  2022  parsers
drwx------   2 sticks sticks       4096 Aug 31 04:15  .password-store
-rw-r--r--   1 sticks sticks        131 Jan  3  2020  .pastebinit.xml
-rw-r--r--   1 sticks sticks      66306 Jun 24  2019  patty_online.html
-rw-r--r--   1 sticks sticks      34759 Dec 31  2019  pdflist
-rw-r--r--   1 sticks sticks       1356 Jun 24  2019  .pgadmin3
drwxr-xr-x   2 sticks sticks       4096 Jun 24  2019  .Phoenicis
-rw-rw-r--   1 sticks sticks      15422 Sep  7  2022  phonelist.txt
-rw-rw-r--   1 sticks sticks     211940 Jan  5  2021  photo_2021-01-05_10-44-48.jpg
-rw-r--r--   1 sticks sticks    4930341 Apr 14  2020  Photos_downloaded_by_AirDroid.zip
drwx------   2 sticks sticks       4096 Aug 31 04:15  Picture
drwx------   8 sticks sticks    1359872 Oct  9 01:19  Pictures
-rw-------   1 sticks sticks      16956 Jul  2  2019  .pine-debug1
-rw-------   1 sticks sticks      23032 Jul  2  2019  .pinerc
drwx------   2 sticks sticks       4096 Aug 31 04:15  .pip
drwx------   2 sticks sticks       4096 Aug 31 04:15  .pipewire-media-session
-rw-r--r--   1 sticks sticks        682 Feb 15  2020  Pipfile.lock
-rw-r--r--   1 sticks sticks     737464 Jun 28  2020  PJD_Booking.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  .pkg-cache
drwx------   3 sticks sticks       4096 Sep 21 22:36  .pki
drwx------   2 sticks sticks       4096 Aug 31 04:15  playerdata
-rw-r--r--   1 sticks sticks        962 Dec 23  2017  playoggs.vlc
-rwxr-xr-x   1 sticks sticks         61 Apr 25  2019  playtrack.sh
-rw-r--r--   1 sticks sticks      12181 Jun 24  2019  plfiles.txt
-rw-r--r--   1 sticks sticks          3 Mar  3  2019  plugin.ini
drwx------   2 sticks sticks       4096 Aug 31 04:15  plugins
-rw-rw-r--   1 sticks sticks     160729 Mar 24  2022 'Pocket - How one hour of slow breathing changed my life.pdf'
-rwxrwxr-x   1 sticks sticks       6393 Jun 19 01:36  pocketsphinx_advanced.py
-rw-rw-r--   1 sticks sticks       3707 Jun 19 01:37  pocketsphinx_guide.md
-rwxrwxr-x   1 sticks sticks       2132 Jun 19 01:34  pocketsphinx_simple.py
drwx------   2 sticks sticks       4096 Aug 31 04:15  .podman-desktop
drwx------   2 sticks sticks       4096 Aug 31 04:15  poi
-rw-r--r--   1 sticks sticks     616869 Aug 30  2020  polar-VTEC_yo-.mp4
drwx------   2 sticks sticks       4096 Aug 31 04:15  practical_vim
-rw-r--r--   1 sticks sticks      22711 Jan 15  2020 'Practice Project.osp'
-rw-rw-r--   1 sticks sticks        291 Apr 15  2024  .profile
-rw-rw-r--   1 sticks sticks        210 Jul  3  2022  .profile_mycroft
drwx------   2 sticks sticks       4096 Aug 31 04:15  Projects
-rwxrwxr-x   1 sticks sticks        170 Jun 20  2023 'Proton Experimental.desktop'
drwx------   2 sticks sticks       4096 Aug 31 04:15  PS4
-rw-rw-r--   1 sticks sticks         73 Nov 20  2023  ps5
-rw-rw-r--   1 sticks sticks       3149 Aug 31  2021  public
drwx------   2 sticks sticks       4096 Aug 31 04:15  Public
-rw-rw-r--   1 sticks sticks       3149 Aug 31  2021  public.1
drwx------   2 sticks sticks       4096 Aug 31 04:15  .pulse
-rw-------   1 sticks sticks        256 Jun 24  2019  .pulse-cookie
drwx------   2 sticks sticks       4096 Aug 31 04:15  .purple
drwx------   2 sticks sticks       4096 Aug 31 04:15  .purple-old
drwx------   2 sticks sticks       4096 Aug 31 04:15  .putty
drwx------   2 sticks sticks       4096 Aug 31 04:15  __pycache__
drwx------   2 sticks sticks       4096 Aug 31 04:15  .pyenv
drwx------   2 sticks sticks       4096 Aug 31 04:15  .pylint.d
drwx------   2 sticks sticks       4096 Aug 31 04:15  .pyrenamer
-rw-------   1 sticks sticks      12890 Nov  2  2024  .pythonhist
-rw-------   1 sticks sticks      22429 Jun  6  2024  .python_history
-rw-r--r--   1 sticks sticks       5673 Jan  3  2020  q
-rw-rw-r--   1 sticks sticks      38514 Dec  5  2021  QRCode_www.paypal.com.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  .r
drwx------   2 sticks sticks       4096 Aug 31 04:15  R
drwx------   2 sticks sticks       4096 Aug 31 04:15  RaceTheSun_Screenshots
drwx------   2 sticks sticks       4096 Aug 31 04:15  RAIDar
-rwxr-x--x   1 sticks sticks    1379510 Jun 24  2019  RAIDar_Linux-4_3_8.sh
-rw-r--r--   1 sticks sticks        199 Nov 11  2019  ramstein-list
-rw-r-----   1 sticks sticks      67967 Jun 24  2019  Ranch_Dressing.jpeg
-rw-r--r--   1 sticks sticks      32489 Sep 17 14:41  README.md
-rw-r--r--   1 sticks sticks     262025 Jun 24  2019  RealPythonPart1Preview-12232016-final.pdf
-rw-r--r--   1 sticks sticks       1912 Jun 24  2019  .recently-used
drwx------   2 sticks sticks       4096 Aug 31 04:15  reddio
drwx------   2 sticks sticks       4096 Aug 31 04:15  .redhat
-rw-r--r--   1 sticks sticks       1260 Jun 24  2019  redpillblack.xml
-rw-r--r--   1 sticks sticks         70 Dec  1  2019  .redshiftgrc
-rw-r--r--   1 sticks sticks        375 Jun 14  2020  regex_characters.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  region
-rwxrwxr-x   1 sticks sticks        593 Feb 17  2025  registry.vdf
-rwxrwxr-x   1 sticks sticks        590 Nov 19  2023  registry.vdf.1958691545.tmp
-rwxrwxr-x   1 sticks sticks        590 May  1  2024  registry.vdf.3444007212.tmp
-rw-rw-r--   1 sticks sticks       1089 Jun 24  2019  Release.key
drwx------   2 sticks sticks       4096 Aug 31 04:15  .remarkable
drwx------   2 sticks sticks       4096 Aug 31 04:15  .remmina
drwx------   2 sticks sticks       4096 Aug 31 04:15  remotewp
-rwxr-xr-x   1 sticks sticks        143 Dec 27  2022  removepars
drwx------   2 sticks sticks       4096 Aug 31 04:15  .repoconfig
-rw-r--r--   1 sticks sticks         94 Mar 11  2016  .repo_.gitconfig.json
drwx------   2 sticks sticks       4096 Aug 31 04:15  repos
drwx------   2 sticks sticks       4096 Aug 31 04:15  resourcepacks
-rw-rw-r--   1 sticks sticks          0 Feb 18  2024  .Rhistory
drwx------   2 sticks sticks       4096 Aug 31 04:15  .ripoff
-rwxr-xr-x   1 sticks sticks       1141 Jan  5  2020  rmapps
-rwxr-xr-x   1 sticks sticks       2884 Nov 16  2019  rmgreeterset
-rwxr-xr-x   1 sticks sticks        215 Jul 28  2019  rmnlohmann
-rw-------   1 sticks sticks       1024 Sep 21 21:29  .rnd
drwx------   2 sticks sticks       4096 Aug 31 04:15  Roms
lrwxrwxrwx   1 sticks sticks         39 Nov 17  2023  root -> /home/sticks/.steam/debian-installation
drwx------   2 sticks sticks       4096 Aug 31 04:15  .ropeproject
drwx------   2 sticks sticks       4096 Aug 31 04:15  .rpmdb
-rw-r--r--   1 sticks sticks  138679947 Jun 24  2019  rsynclog.txt
drwx------   6 sticks sticks       4096 Aug 31 04:15  .rustup
drwx------   2 sticks sticks       4096 Aug 31 04:15  rwxrob
drwx------   2 sticks sticks       4096 Aug 31 04:15  rwxrob_scripts
-rw-rw-r--   1 sticks sticks    1435724 Jan 20  2024  s
drwx------   2 sticks sticks       4096 Aug 31 04:15  .sane
drwx------   2 sticks sticks       4096 Aug 31 04:15  saves
drwx------   2 sticks sticks       4096 Aug 31 04:15  .sbd
-rw-rw-r--   1 sticks sticks     519113 Oct 11  2021 'Scanned Document1.pdf'
drwx------   2 sticks sticks       4096 Aug 31 04:15  .scratch
-rw-r--r--   1 sticks sticks       3729 Apr 26  2020  .screenrc
drwx------   2 sticks sticks       4096 Aug 31 04:15  .screenstudio
drwx------   2 sticks sticks       4096 Aug 31 04:15  .scribus
-rw-------   1 sticks sticks         11 May 30  2023  .sdcv_history
lrwxrwxrwx   1 sticks sticks         47 Nov 17  2023  sdk32 -> /home/sticks/.steam/debian-installation/linux32
lrwxrwxrwx   1 sticks sticks         47 Nov 17  2023  sdk64 -> /home/sticks/.steam/debian-installation/linux64
-rwxr-xr-x   1 sticks sticks         57 Jun 24  2019  sd.sh
-rw-------   1 sticks sticks         66 Jun 24  2019  .selected_editor
-rw-rw-rw-   1 sticks sticks        702 Dec 18  2022  send2jim.py
drwx------   2 sticks sticks       4096 Aug 31 04:15  serverconfig
-rw-rw-r--   1 sticks sticks       1350 Feb 16  2023  server.properties
drwx------   2 sticks sticks       4096 Aug 31 04:15  server-resource-packs
-rw-r--r--   1 sticks sticks         86 Oct  9  2020  servers.dat_old
-rw-r--r--   1 sticks sticks       1015 Jun 24  2019  Service_Appointment.vcs
-rw-r--r--   1 sticks sticks          3 Oct  9  2020  session.lock
-rw-rw-r--   1 sticks sticks       5268 Dec 25  2023  setup-repos.sh
-rw-rw-r--   1 sticks sticks  451372892 Nov 27  2023 'S - FC Cincinnati - MLS Press Conference 2023-11-27 13_17 [1OdKrjkAjplKX].mp4'
-rw-r--r--   1 sticks sticks       2187 Dec 26  2019  sha256.txt
drwx------  40 sticks sticks       4096 Oct  1 03:21  share
-rw-r--r--   1 sticks sticks         14 Oct 26  2020  .shell.pre-oh-my-zsh
-rw-r--r--   1 sticks sticks     513330 Aug  1  2020  shldnt_have_to.png
-rw-rw-r--   1 sticks sticks        264 Jan  6  2024 'Shotwell Import Log.txt'
drwx------   2 sticks sticks       4096 Aug 31 04:15  .shutter
drwx------   2 sticks sticks       4096 Aug 31 04:15  signal-export
drwx------   2 sticks sticks       4096 Aug 31 04:15  SII_Decrypt
drwx------   2 sticks sticks       4096 Aug 31 04:15  simple_screen_reader
-rw-r--r--   1 sticks sticks        166 Jun 24  2019  skellist
-rw-rw-r--   1 sticks sticks    3283897 Jan 20  2025  Skull_Door.mp4
drwx------   9 sticks sticks       4096 Feb 15  2023  .Skype
drwx------   2 sticks sticks       4096 Aug 31 04:15  slim-containers
-rw-r--r--   1 sticks sticks     770074 Jul 29  2020  smart_congress.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  .smb
-rw-rw-r--   1 sticks sticks         54 Jul 26  2022  .smbcred
-rw-------   1 sticks sticks         35 Sep 24 05:34  .smbcredentials
-rwxr-xr-x   1 sticks sticks         59 Jun 24  2019  .smbcreds
-rw-r--r--   1 sticks sticks     159456 Dec 21  2019  sm_Xmas_Shell_Sticks.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  snap
-rw-r--r--   1 sticks sticks   22520698 Jun 24  2019  Songify_This-Winning-a_Song_by_Charlie_Sheen-9QS0q3mGPGg.mp4
drwx------   2 sticks sticks       4096 Aug 31 04:15  SoundClips
-rw-rw-r--   1 sticks sticks       2136 Jun 24  2019  sounds.txt
-rw-r--r--   1 sticks sticks         23 Jun 19  2020  spawnpoint.txt
-rw-rw-r--   1 sticks sticks      21413 Sep 28  2020  spcthc.svg
drwx------   2 sticks sticks       4096 Aug 31 04:15  .speech-dispatcher
drwx------   2 sticks sticks       4096 Aug 31 04:15  Spigot
-rw-rw-r--   1 sticks sticks   35764481 Oct  9  2020  spigot-1.16.3.jar
drwx------   2 sticks sticks       4096 Aug 31 04:15  .spotdl
-rwxr-xr-x   1 sticks sticks  121005248 Oct  7  2022  Spotify-x86_64.AppImage
-rw-rw-r--   1 sticks sticks    4785898 Apr 25  2022  Spring-2022-Shoreline-Digital.pdf
drwx------   2 sticks sticks       4096 Aug 31 04:15  src
lrwxrwxrwx   1 sticks sticks         11 Jun 11  2019  srv_music -> /mnt/music/
lrwxrwxrwx   1 sticks sticks         12 Jun 11  2019  srv_video -> /mnt/videos/
drwx------   2 sticks sticks       4096 Oct  7 04:06  .ssh
drwx------   2 sticks sticks       4096 Aug 31 04:15  .ssr
drwx------   2 sticks sticks       4096 Aug 31 04:15 'Standard Notes Backups'
drwx------   2 sticks sticks       4096 Aug 31 04:15  .stardict
lrwxrwxrwx   1 sticks sticks         32 Nov  2  2022  starship.toml -> .dotfiles/starship/starship.toml
-rwxr-xr-x   1 sticks sticks         46 Jun 24  2019  .start-conky
drwx------   8 sticks sticks       4096 Sep 29 21:00  state
drwx------   2 sticks sticks       4096 Aug 31 04:15  stats
-rwxr-xr-x   1 sticks sticks       1582 Jun 24  2019  stay_rolling_jk.sh
drwxrwxr-x   3 sticks sticks       4096 Oct  8 22:36  .steam
lrwxrwxrwx   1 sticks sticks         39 Nov 17  2023  steam -> /home/sticks/.steam/debian-installation
lrwxrwxrwx   1 sticks sticks         13 Jun 24  2023  steamcmd -> ./steamcmd.sh
-rw-rw-rw-   1 sticks sticks    2428561 Jan  4  2018  steamcmd_linux.tar.gz
-rwxrw-r--   1 sticks sticks       1166 Jan  4  2018  steamcmd.sh
-rwxrwxr-x   1 sticks sticks        179 Jul  7  2023 'Steam Linux Runtime - Sniper.desktop'
lrwxrwxrwx   1 sticks sticks         31 Oct  8 18:35  .steampath -> /home/sticks/.steam/sdk32/steam
lrwxrwxrwx   1 sticks sticks         29 Oct  8 18:35  .steampid -> /home/sticks/.steam/steam.pid
-rw-rw-r--   1 sticks sticks          5 Feb 17  2025  steam.pid
prw-------   1 sticks sticks          0 Apr 12  2024  steam.pipe
-rw-r--r--   1 sticks sticks          0 Aug 15  2023  sticksbackup.timer
-rw-r--r--   1 sticks sticks        187 Jun 24  2019  Sticks.key
-rw-rw-rw-   1 sticks sticks       4246 Jun  8  2023  sticks@kidpc
-rw-r--r--   1 sticks sticks       1418 Jun 20  2023  sticks@kidspc
-rw-r--r--   1 sticks sticks        519 Jun 11  2020  sticks@minecraft.stickskilbane.com
-rw-rw-r--   1 sticks sticks    1506428 Sep  5  2021  sticks.mp4
-rw-r--r--   1 sticks sticks        519 Jun 11  2020  sticks@nicksmc.stickskilbane.com
drwx------   2 sticks sticks       4096 Aug 31 04:15  .stremio-server
drwx------   2 sticks sticks       4096 Aug 31 04:15  .subversion
-rw-r--r--   1 sticks sticks          0 Feb 15  2023  .sudo_as_admin_successful
-rw-r--r--   1 sticks sticks        609 Jun 24  2019  .swfinfo
-rw-------   1 sticks sticks      53248 Jun 24  2019  .swm
-rw-------   1 sticks sticks      57344 Jun 24  2019  .swn
-rw-------   1 sticks sticks      12288 Jun 24  2019  .swo
drwx------   2 sticks sticks       4096 Aug 31 04:15  .swt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .synaptic
-rw-rw-r--   1 sticks sticks          0 Oct  4  2024  sys
-rw-r--r--   1 sticks sticks     752619 Nov 12  2020  system76-logs.tgz
drwx------   2 sticks sticks       4096 Aug 31 04:15  systemd
-rw-rw-r--   1 sticks sticks      63856 Aug 30  2022  systemd.pdf
drwx------   2 sticks sticks       4096 Aug 31 04:15 'Team Drives'
drwx------   2 sticks sticks       4096 Aug 31 04:15  Team_Drives
drwx------   2 sticks sticks       4096 Aug 31 04:15  .teamviewer
-rw-rw-r--   1 sticks sticks     352092 Dec 21  2023  Tech_Lepracaun
-rw-rw-r--   1 sticks sticks     352092 Dec 21  2023  Tech_Lepracaun.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  .telegram-cli
-rw-rw-r--   1 sticks sticks        347 Feb  7  2021  telegram_invite.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  telegram_stream
drwx------   2 sticks sticks       4096 Aug 31 04:15  temp
-rwxrwxr-x   1 sticks sticks       3718 Jun  2 00:28  temp_cifs_share.sh
-rw-r--r--   1 sticks sticks       1897 Jun 24  2019  Temp.ipynb
drwx------   2 sticks sticks       4096 Aug 31 04:15  Templates
-rw-rw-r--   1 sticks sticks       1580 Nov 21  2020  temp.md
drwxrwxr-x   2 sticks sticks       4096 Sep 22 20:01  temp_png_edit
-rwxrwxr-x   1 sticks sticks       3797 Jun  2 00:23  temp_samba_share.sh
-rw-r--r--   1 sticks sticks         98 Jun 24  2019  Temp.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  test
-rwxrwxr-x   1 sticks sticks        644 Oct  2 01:36  test_fzf_history.sh
-rw-rw-r--   1 sticks sticks        292 Jul 16  2022  test.jpg
-rw-r--r--   1 sticks sticks         21 Nov 22  2020  test.md
-rw-r--r--   1 sticks sticks     415065 Aug  7  2020  test.mkv
-rw-r--r--   1 sticks sticks     639476 Aug  7  2020  test.mp4
-rw-r--r--   1 sticks sticks         13 Jun 24  2019  test.sh
-rw-r--r--   1 sticks sticks          7 Jun 24  2019  test.vi
-rw-r--r--   1 sticks sticks      64044 Jul  7 12:39  test.wav
drwx------   2 sticks sticks       4096 Aug 31 04:15  .texlive2017
-rw-rw-r--   1 sticks sticks       2128 Jun 24  2019  text16.png
-rw-r--r--   1 sticks sticks       1111 Jan  7  2020  theliofstab
drwx------   2 sticks sticks       4096 Aug 31 04:15  theliohome
drwx------   2 sticks sticks       4096 Aug 31 04:15  .themes
-rw-rw-r--   1 sticks sticks       9855 Jun 24  2021  thmzolefc2771.png
drwx------   2 sticks sticks       4096 Aug 31 04:15  thumbnail
drwx------   2 sticks sticks       4096 Aug 31 04:15  .thumbnails
drwx------   2 sticks sticks       4096 Aug 31 04:15  .thunderbird
-rw-r--r--   1 sticks sticks   73429835 Jun 24  2019  Thunderstruck.mp4
-rw-------   1 sticks sticks          4 Sep  6  2020  .tig_history
drwx------   2 sticks sticks       4096 Aug 31 04:15  TIPP10
drwx------   2 sticks sticks       4096 Aug 31 04:15  .tmp
drwx------   2 sticks sticks       4096 Aug 31 04:15  .tmux
-rw-rw-r--   1 sticks sticks      12914 Jul  1  2021  tmuxcommands.txt
lrwxrwxrwx   1 sticks sticks         25 Dec 17  2021  .tmux.conf -> .dotfiles/tmux/.tmux.conf
drwx------   2 sticks sticks       4096 Aug 31 04:15  .tmuxinator
-rw-rw-r--   1 sticks sticks       1979 Jul 19  2021  .tmux-live.conf
-rwxr-xr-x   1 sticks sticks        336 Jun 29  2017  toggle_term
-rw-r--r--   1 sticks sticks        433 Jun 24  2019  translog.20160619171551.log
-rw-r--r--   1 sticks sticks      32348 Jun 24  2019  translog.20160619172332.log
drwx------   2 sticks sticks       4096 Aug 31 04:15  trek_sounds
-rw-rw-r--   1 sticks sticks       3728 Jun 18  2024  trixies_Trailer
drwx------   2 sticks sticks       4096 Aug 31 04:15  tuir
drwx------   2 sticks sticks       4096 Aug 31 04:15 'Turbo Tax'
drwx------   2 sticks sticks       4096 Aug 31 04:15  Turbo_Tax
drwx------   2 sticks sticks       4096 Aug 31 04:15  .tuxpaint
drwx------   2 sticks sticks       4096 Aug 31 04:15  TV
-rw-r--r--   1 sticks sticks     231178 Aug  6  2020  u35kNTQE.jpeg
-rw-r--r--   1 sticks sticks        187 Jun 24  2019  ubuntu-Mate64-Hash.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .ubuntuone
-rw-r--r--   1 sticks sticks        660 Jun 24  2019  ubunuinstall.sh
drwx------   2 sticks sticks       4096 Aug 31 04:15  ui
drwx------   2 sticks sticks       4096 Aug 31 04:15  UltiSnips
drwx------   2 sticks sticks       4096 Aug 31 04:15  .uml
drwx------   2 sticks sticks       4096 Aug 31 04:15  Unknown
-rw-rw-r--   1 sticks sticks      14022 Sep 25 18:34  Untitled
-rw-r--r--   1 sticks sticks       2406 Jun 24  2019  Untitled2.ipynb
-rw-r--r--   1 sticks sticks         72 Sep  8  2020  Untitled4.ipynb
-rw-r--r--   1 sticks sticks         39 Oct  1  2021  Untitled_Document.sh
-rw-r--r--   1 sticks sticks        826 Jun 24  2019  Untitled.ipynb
-rw-r--r--   1 sticks sticks        528 Apr 21  2020 'Upcoming Appointment.ics'
drwx------   2 sticks sticks       4096 Oct  9 00:11  updatelogs
-rw-rw-r--   1 sticks sticks      10970 Aug  4 21:39  update_output.txt
-rw-r--r--   1 sticks sticks        271 Jun 24  2019  upgrade17-1_17-2.txt
drwx------   2 sticks sticks       4096 Aug 31 04:15  .urserver
drwx------   2 sticks sticks       4096 Aug 31 04:15  .urxvt
drwx------   3 sticks sticks       4096 Apr  1  2021  .var
-rw-rw-r--   1 sticks sticks       3351 Oct  9  2023  VDHanson_Take_On_Israel_Hommas
drwx------   2 sticks sticks       4096 Aug 31 04:15  ventoy-1.0.89
drwx------   2 sticks sticks       4096 Aug 31 04:15  .venv
-rw-r--r--   1 sticks sticks   29994526 Aug 27  2017  venv35.tar.bz2
-rw-r--r--   1 sticks sticks    6153114 Sep  1  2022 'Verification video [55620245].mp4'
drwx------   2 sticks sticks       4096 Aug 31 04:15  versions
-rw-r--r--   1 sticks sticks         65 Oct  9  2020  versions.sum
-rw-rw-r--   1 sticks sticks       4090 Jun  8 17:52  vic.md
-rw-r--r--   1 sticks sticks    4172581 Jun 24  2019  VID_20170429_153716-ANIMATION.gif
drwx------   7 sticks sticks      20480 Oct  7 18:33  Videos
drwx------   2 sticks sticks       4096 Oct  1 23:08  .vim
-rw-rw-r--   1 sticks sticks       3979 Jun 24  2019  vim-classes-master.zip
drwx------   2 sticks sticks       4096 Aug 31 04:15  vim-fubitive
-rw-------   1 sticks sticks      28451 Oct  3 23:52  .viminfo
-rw-------   1 sticks sticks       1076 Jan  6  2020  .viminfo.tmp
-rw-------   1 sticks sticks       4096 Nov 24  2017  .viminfu.tmp
-rw-rw-r--   1 sticks sticks       5782 Nov 23  2020  vimkeys
-rw-r--r--   1 sticks sticks       2145 Jun 24  2019  vim.log
-rw-rw-rw-   1 sticks sticks        102 Dec 28  2022  vim.out
-rw-rw-rw-   1 sticks sticks         20 Dec 28  2022  vim.output
drwx------   2 sticks sticks       4096 Aug 31 04:15  .vimplugins
lrwxrwxrwx   1 sticks sticks         21 Nov  2  2021  .vimrc -> .config/nvim/init.vim
-rw-r--r--   1 sticks sticks       4649 Jun 24  2019  .vimrc-1.bak
-rw-r--r--   1 sticks sticks         82 Aug 24  2017  .vimrc.bundles.local
-rw-r--r--   1 sticks sticks       1413 Jun 24  2019  .vimrc.old
drwx------   2 sticks sticks       4096 Oct 16  2020  .VirtualBox
drwx------   2 sticks sticks       4096 Aug 31 04:15  .visualvm
drwx------   2 sticks sticks       4096 Aug 31 04:15  vivaldi
drwx------   2 sticks sticks       4096 Aug 31 04:15  vm-share
drwx------   2 sticks sticks       4096 Aug 31 04:15  vmwkitmp
drwx------   2 sticks sticks       4096 Aug 31 04:15  .vnc
drwx------   2 sticks sticks       4096 Aug 31 04:15  vpn_configs
drwx------   2 sticks sticks       4096 Aug 31 04:15  .vscode
drwx------   2 sticks sticks       4096 Aug 31 04:15  .vscode-insiders
drwx------   2 sticks sticks       4096 Aug 31 04:15  .vscode-oss
drwxrwxr-x   2 sticks sticks       4096 Jun 24  2019  .VSCodeVim
drwx------   2 sticks sticks       4096 Aug 31 04:15  .w3m
drwx------   2 sticks sticks       4096 Aug 31 04:15  .wallch
drwx------   2 sticks sticks       4096 Aug 31 04:15  .wallpaperdownloader
drwx------   2 sticks sticks       4096 Aug 31 04:15  Wallpapers
drwx------   2 sticks sticks       4096 Aug 31 04:15  .warp
-rw-r--r--   1 sticks sticks         35 Jun  5  2023  wassup
drwx------   2 sticks sticks       4096 Aug 31 04:15  .weather
drwx------   2 sticks sticks       4096 Aug 31 04:15  webcache
drwx------   2 sticks sticks       4096 Aug 31 04:15  Webcam_Pictures
drwx------   2 sticks sticks       4096 Aug 31 04:15  .weechat
drwx------   2 sticks sticks       4096 Aug 31 04:15  welcome-to-docker
-rw-r--r--   1 sticks sticks       1076 Oct  5 00:20  .wget-hsts
-rw-r--r--   1 sticks sticks        738 Feb 10  2024  wget-log
-rw-r--r--   1 sticks sticks      94359 Nov  8  2019  WhiteOnBlack_Logo.png
-rw-r--r--   1 sticks sticks      61302 Nov  8  2019  WhiteOnBlack_Logo.xcf
-rw-r--r--   1 sticks sticks      65735 Jun 24  2019  wincar.jpg
-rw-r--r--   1 sticks sticks         80 Oct  9  2020  window_settings_launcher.conf
drwx------   2 sticks sticks       4096 Aug 31 04:15  .wine
drwx------   2 sticks sticks       4096 Aug 31 04:15  .wingide5
drwx------   2 sticks sticks       4096 Aug 31 04:15  .wireshark
drwx------   2 sticks sticks       4096 Aug 31 04:15  world
drwx------   2 sticks sticks       4096 Aug 31 04:15  world_nether
drwx------   2 sticks sticks       4096 Aug 31 04:15  world_the_end
-rw-rw-r--   1 sticks sticks     127117 Sep 25 15:13  wps-office_11.1.0.8767_amd64.deb
-rwxr-xr-x   1 sticks sticks        445 Jun  3 22:09  wps-office-prometheus.desktop
-rw-rw-r--   1 sticks sticks        225 Jul  2  2023  :wq
-rwxrwxr-x   1 sticks sticks        325 Aug  2 21:00  WTAssetViewer.desktop
-rwxrwxr-x   1 sticks sticks        327 Aug  2 21:00  WTMissionEditor.desktop
lrwxrwxrwx   1 sticks sticks         77 Sep 26  2022  WT_Replays -> '/home/sticks/.steam/debian-installation/steamapps/common/War Thunder/Replays/'
lrwxrwxrwx   1 sticks sticks         80 Oct 23  2023  WT_Screenshots -> '/home/sticks/.steam/debian-installation/steamapps/common/War Thunder/Screenshots'
lrwxrwxrwx   1 sticks sticks         82 Jul 31  2023  WT_User_Missions -> '/home/sticks/.steam/debian-installation/steamapps/common/War Thunder/UserMissions/'
drwx------   2 sticks sticks       4096 Aug 31 04:15  .x2go
drwx------   2 sticks sticks       4096 Aug 31 04:15  .x2goclient
-rw-rw-rw-   1 sticks sticks    1365286 Mar 11  2023 'Xaeros_Minimap_23.3.0_Fabric_1.19.3 (1).jar'
-rw-------   1 sticks sticks        327 Sep 15  2020  .Xauthority
-rw-------   1 sticks sticks        164 Jun 24  2019  .Xauthority.bak
drwx------   2 sticks sticks       4096 Aug 31 04:15  .xchat2
drwx------   2 sticks sticks       4096 Aug 31 04:15  xfconf
drwx------   2 sticks sticks       4096 Aug 31 04:15  .xine
-rw-r--r--   1 sticks sticks        281 Sep 27  2021  .xinitrc
-rw-r--r--   1 sticks sticks     354095 Dec 21  2019  Xmas_Shell_Sticks.png
-rw-r--r--   1 sticks sticks       5501 Apr 26  2020  .Xresources
-rw-r--r--   1 sticks sticks         67 Apr 26  2020  .xsession
-rw-------   1 sticks sticks       7269 Sep 15  2020  .xsession-errors
-rw-------   1 sticks sticks       9524 Sep 15  2020  .xsession-errors.old
-rw-r--r--   1 sticks sticks        516 Apr 26  2020  .xsessionrc
-rw-rw-r--   1 sticks sticks       5177 Apr 17  2023  xvids.keep
drwx------   2 sticks sticks       4096 Aug 31 04:15  .xwelltris
drwx------   2 sticks sticks       4096 Aug 31 04:15  .yarn
-rw-r--r--   1 sticks sticks        116 Dec 26  2022  .yarnrc
drwxrwxr-x  35 sticks sticks       4096 Oct  1 22:52  yazi
drwx------   2 sticks sticks       4096 Aug 31 04:15  youtube-dl
-rw-rw-r--   1 sticks sticks      49626 Oct  1 23:32  .zcompdump
-rw-rw-r--   1 sticks sticks      51147 Oct  5 00:30  .zcompdump-thelio-5.8.1
drwx------   2 sticks sticks       4096 Sep  6 12:00  .zcompdump-thelio-5.8.1.lock
-r--r--r--   1 sticks sticks     118640 Sep  3 21:40  .zcompdump-thelio-5.8.1.zwc
-rw-r--r--   1 sticks sticks       7764 Nov  4  2019  Zeb-temp
drwx------   2 sticks sticks       4096 Aug 31 04:15  .zenmap
drwx------   4 sticks sticks      20480 Oct  9 00:51  zets
drwx------   2 sticks sticks       4096 Aug 31 04:15  zets-tmp
drwxrwxr-x   3 sticks sticks      16384 Oct  9 01:17  zetswiki
drwx------   2 sticks sticks       4096 Aug 31 04:15  .zoom
-rw-rw-rw-   1 sticks sticks          0 Apr 15  2024  .zprofile
-rw-rw-r--   1 sticks sticks         21 Jul 16  2022  .zshenv
-rw-------   1 sticks sticks     612216 Oct  9 01:19  .zsh_history
-rw-rw-r--   1 sticks sticks        663 Oct  2 01:28  .zshrc
-rw-rw-r--   1 sticks sticks        128 Jun 21 22:56  .zshrc---
lrwxrwxrwx   1 sticks sticks         23 Sep 27 22:53  .zshrc.backup -> /home/sticks/bin/.zshrc
-rw-r--r--   1 sticks sticks       4194 Sep 22 22:28  .zshrc.bck
lrwxrwxrwx   1 sticks sticks         32 Oct  2 00:28  .zshrc-personal -> /home/sticks/bin/.zshrc-personal
lrwxrwxrwx   1 sticks sticks         32 Sep 27 22:53  .zshrc-personal.backup -> /home/sticks/bin/.zshrc-personal
-rw-rw-r--   1 sticks sticks       4284 Sep 21 22:23  .zshrc.pre-oh-my-zsh
-rw-r--r--   1 sticks sticks       9368 Oct 24  2020  .zshrc.pre-oh-my-zsh-2025-09-21_18-36-39
-rw-r--r--   1 sticks sticks       9368 Oct 24  2020  .zshrc.pre-oh-my-zsh-2025-09-21_22-25-13
```

I can see you have a `zets` directory and a `zetswiki` directory. Let me check if there's an existing git repository in one of these:

**Command Executed:**
```bash
ls -la zets
```

**Output:**
```
total 76
drwx------   4 sticks sticks 20480 Oct  9 00:51 .
drwx------ 438 sticks sticks 36864 Oct  9 01:19 ..
drwxrwxr-x   8 sticks sticks  4096 Oct  8 20:53 .git
-rw-rw-r--   1 sticks sticks   624 Oct  1 21:54 .gitignore
drwxrwxr-x   3 sticks sticks  4096 Oct  1 21:54 .obsidian
-rw-rw-r--   1 sticks sticks   211 Oct  1 21:54 .vimwiki_tags
```


**Command Executed:**
```bash
ls -la zetswiki
```

**Output:**
```
total 1652
drwxrwxr-x   3 sticks sticks  16384 Oct  9 01:17  .
drwx------ 438 sticks sticks  36864 Oct  9 01:19  ..
-rw-rw-r--   1 sticks sticks     98 Oct  1 21:54  202109272105-docker_detach.md
-rw-rw-r--   1 sticks sticks    788 Oct  1 21:54  202109272215-positional_params.md
-rw-rw-r--   1 sticks sticks    701 Oct  1 21:54  202109282208-backup_codes.md
-rw-rw-r--   1 sticks sticks     84 Oct  1 21:54  202109282242-Change_git_master_to_main.md
-rw-rw-r--   1 sticks sticks    326 Oct  1 21:54  202109282247-congressional_races.md
-rw-rw-r--   1 sticks sticks     79 Oct  1 21:54  202109282307-discord_link.md
-rw-rw-r--   1 sticks sticks    430 Oct  1 21:54  202109282315-google_backup_codes.md
-rw-rw-r--   1 sticks sticks    323 Oct  1 21:54  202109282320-keyboard_backlight.md
-rw-rw-r--   1 sticks sticks    656 Oct  1 21:54  202109282326-mc_coordinates.md
-rw-rw-r--   1 sticks sticks    145 Oct  1 21:54  202109282356-mastodon_links.md
-rw-rw-r--   1 sticks sticks    191 Oct  1 21:54  202109290000-matrix_invite_links.md
-rw-rw-r--   1 sticks sticks    120 Oct  1 21:54  202109290002-minecraft_flatpak_path.md
-rw-rw-r--   1 sticks sticks    120 Oct  1 21:54  202109290004-rtfm.md
-rw-rw-r--   1 sticks sticks    449 Oct  1 21:54  202109290005-pop_os_links.md
-rw-rw-r--   1 sticks sticks    179 Oct  1 21:54  202109290007-python_githubs.md
-rw-rw-r--   1 sticks sticks    846 Oct  1 21:54  202109290009-reasons_against_mask_mandates.md
-rw-rw-r--   1 sticks sticks    165 Oct  1 21:54  202109290011-regex_email.md
-rw-rw-r--   1 sticks sticks    216 Oct  1 21:54  202109290051-Shot_At_Panico.md
-rw-rw-r--   1 sticks sticks     84 Oct  1 21:54  202109290052-Telegram_Client.md
-rw-rw-r--   1 sticks sticks  25521 Oct  1 21:54  202109290052-Vim_Keybindings.md
-rw-rw-r--   1 sticks sticks    123 Oct  1 21:54  202109290053-VivaBarnes_urls.md
-rw-rw-r--   1 sticks sticks    155 Oct  1 21:54  202109290145-backup_command.md
-rw-rw-r--   1 sticks sticks     74 Oct  1 21:54  202109290153-vwpractice.md
-rw-rw-r--   1 sticks sticks    292 Oct  1 21:54  202109290327-rwxrob_vi_help.md
-rw-rw-r--   1 sticks sticks    153 Oct  1 21:54  202109290358-htop_enable_f10.md
-rw-rw-r--   1 sticks sticks    238 Oct  1 21:54  202109290507-microsoft_minecraft_recovery_codes.md
-rw-rw-r--   1 sticks sticks    127 Oct  1 21:54  202109290511-keybase_key.md
-rw-rw-r--   1 sticks sticks    756 Oct  1 21:54  202109290516-urls.md
-rw-rw-r--   1 sticks sticks    116 Oct  1 21:54  202109290519-install_spice_guest_editions.md
-rw-rw-r--   1 sticks sticks    129 Oct  1 21:54  202109290524-nanas_room_invite_link.md
-rw-rw-r--   1 sticks sticks    143 Oct  1 21:54  202110010924-bash_loop_counter_example.md
-rw-rw-r--   1 sticks sticks    123 Oct  1 21:54  202110020936-minecraft_recovery_code.md
-rw-rw-r--   1 sticks sticks     96 Oct  1 21:54  202110061738-delta_chat.md
-rw-rw-r--   1 sticks sticks    178 Oct  1 21:54  202110071008-hothead_order.md
-rw-rw-r--   1 sticks sticks     82 Oct  1 21:54  202110112102-open_all_files_in_dir_zsh_vim.md
-rw-rw-r--   1 sticks sticks    458 Oct  1 21:54  202110130136-music_list.md
-rw-rw-r--   1 sticks sticks    108 Oct  1 21:54  202110191912-Delete_Trailing_Space_In_Vim.md
-rw-rw-r--   1 sticks sticks    512 Oct  1 21:54  202110192032-vim_movements.md
-rw-rw-r--   1 sticks sticks    155 Oct  1 21:54  202110201324-incremented_numbers_in_vim.md
-rw-rw-r--   1 sticks sticks  86695 Oct  1 21:54  202110211332-online-Learning-resourses.md
-rw-rw-r--   1 sticks sticks    829 Oct  1 21:54  202110241611-extract_cookies_code.md
-rw-rw-r--   1 sticks sticks    129 Oct  1 21:54  202110301634-vim_special_buffers.md
-rw-rw-r--   1 sticks sticks     73 Oct  1 21:54  202110311229-last_boost.md
-rw-rw-r--   1 sticks sticks     79 Oct  1 21:54  202111011041-rittenhouse.md
-rw-rw-r--   1 sticks sticks    116 Oct  1 21:54  202111031851-vim-ignore-noignore-case.md
-rw-rw-r--   1 sticks sticks     92 Oct  1 21:54  202111081451-display_vi_or_emacs_mode.md
-rw-rw-r--   1 sticks sticks    428 Oct  1 21:54  202111151249-vim_registers.md
-rw-rw-r--   1 sticks sticks    136 Oct  1 21:54  202111232018-petlab.md
-rw-rw-r--   1 sticks sticks    127 Oct  1 21:54  202111262352-papaws_menu.md
-rw-rw-r--   1 sticks sticks     77 Oct  1 21:54  202111291632-personal_measurements.md
-rw-rw-r--   1 sticks sticks    171 Oct  1 21:54  202112141206-fix_pop_upgrade_daemon.md
-rw-rw-r--   1 sticks sticks     99 Oct  1 21:54  202112310011-brunch_list.md
-rw-rw-r--   1 sticks sticks    226 Oct  1 21:54  202201031007-bitwarden_api.md
-rw-rw-r--   1 sticks sticks    305 Oct  1 21:54  202201221505-quotes.md
-rw-rw-r--   1 sticks sticks    225 Oct  1 21:54  202201281319-gnome_move_window_to_workspace_x.md
-rw-rw-r--   1 sticks sticks     55 Oct  1 21:54  202201281835-bitbucket_recovery_codes.md
-rw-rw-r--   1 sticks sticks    159 Oct  1 21:54  202202041615-mincraft_seed_range.md
-rw-rw-r--   1 sticks sticks    142 Oct  1 21:54  202202051522-disable_ipv6.md
-rw-rw-r--   1 sticks sticks    212 Oct  1 21:54  202202121619-thelio_virtualization.md
-rw-rw-r--   1 sticks sticks    109 Oct  1 21:54  202202161217-remove_spaces_in_filenames.md
-rw-rw-r--   1 sticks sticks     62 Oct  1 21:54  202202161713-date_standards.md
-rw-rw-r--   1 sticks sticks    477 Oct  1 21:54  202202181444Z-gnome-keybindings_screenshots.md
-rw-rw-r--   1 sticks sticks     80 Oct  1 21:54  202203081546-nanas_chromebook.md
-rw-rw-r--   1 sticks sticks    134 Oct  1 21:54  202203091842-minecraft_seeds.md
-rw-rw-r--   1 sticks sticks    158 Oct  1 21:54  202203111505-fish_fry.md
-rw-rw-r--   1 sticks sticks     78 Oct  1 21:54  202203141736-vim-write_file_as_sudo.md
-rw-rw-r--   1 sticks sticks   1132 Oct  1 21:54  202203171811-mknetaccts.md
-rw-rw-r--   1 sticks sticks    124 Oct  1 21:54  202203271645-rwx_bangers.md
-rw-rw-r--   1 sticks sticks     81 Oct  1 21:54  202203271659-replace_space_with_n.md
-rw-rw-r--   1 sticks sticks     92 Oct  1 21:54  202203301925-print_local_time_in_tz.md
-rw-rw-r--   1 sticks sticks     77 Oct  1 21:54  202204080549-bash_files_sort_by.md
-rw-rw-r--   1 sticks sticks     91 Oct  1 21:54  202204221203-madis_realname.md
-rw-rw-r--   1 sticks sticks    497 Oct  1 21:54  202204280308-Movies.md
-rw-rw-r--   1 sticks sticks    105 Oct  1 21:54  202205032319-vimwiki_commands_keybinds.md
-rw-rw-r--   1 sticks sticks    122 Oct  1 21:54  202205032345-notify-send.md
-rw-rw-r--   1 sticks sticks    206 Oct  1 21:54  20220505192926-github-recovery-codes.md
-rw-rw-r--   1 sticks sticks    189 Oct  1 21:54  202205090044-list_linux_tz.md
-rw-rw-r--   1 sticks sticks    226 Oct  1 21:54  202205161429-incogni-surfshark_reply.md
-rw-rw-r--   1 sticks sticks    224 Oct  1 21:54  202205211352-jankowicz-joke-post.md
-rw-rw-r--   1 sticks sticks    174 Oct  1 21:54  202205231234-dr_spiegel_jd_post.md
-rw-rw-r--   1 sticks sticks    152 Oct  1 21:54  202205231240-3rd_obama_admin.md
-rw-rw-r--   1 sticks sticks    210 Oct  1 21:54  202205231626-brcc-jokes.md
-rw-rw-r--   1 sticks sticks    126 Oct  1 21:54  202205261355-beto_jokes.md
-rw-rw-r--   1 sticks sticks    420 Oct  1 21:54  202205301435-royalty-free-tracks.md
-rw-rw-r--   1 sticks sticks    327 Oct  1 21:54  202205302223-bearded_butchers_links.md
-rw-rw-r--   1 sticks sticks    115 Oct  1 21:54  202206031453-pipewire_s76.md
-rw-rw-r--   1 sticks sticks     83 Oct  1 21:54  202206121321-self_2022.md
-rw-rw-r--   1 sticks sticks    536 Oct  1 21:54  202206121908-bluetoothctl_commands.md
-rw-rw-r--   1 sticks sticks    412 Oct  1 21:54  202206141856-vim-insert-edit-mappings.md
-rw-rw-r--   1 sticks sticks    166 Oct  1 21:54  202207022215-mycroft_links.md
-rw-rw-r--   1 sticks sticks   4303 Oct  1 21:54  202207192250-jq_examples.md
-rw-rw-r--   1 sticks sticks  42987 Oct  1 21:54  20220722054849-MPV_EXAMPLES.md
-rw-rw-r--   1 sticks sticks  12238 Oct  1 21:54  202207281711-vim-cheat-sheet.md
-rw-rw-r--   1 sticks sticks    233 Oct  1 21:54  202208090920-sound_issues.md
-rw-rw-r--   1 sticks sticks   3783 Oct  1 21:54  20220817190231-zathura_keybinds.md
-rw-rw-r--   1 sticks sticks    254 Oct  1 21:54  202209071245-regexs.md
-rw-rw-r--   1 sticks sticks    145 Oct  1 21:54  202209150930-Remove_Chrome.md
-rw-rw-r--   1 sticks sticks    155 Oct  1 21:54  202209191628-shell_commands.md
-rw-rw-r--   1 sticks sticks   3940 Oct  1 21:54  202209201116-vimcheat.md
-rw-rw-r--   1 sticks sticks    118 Oct  1 21:54  202209211459-war_thunder_invite.md
-rw-rw-r--   1 sticks sticks     92 Oct  1 21:54  202210061645-video_links.md
-rw-rw-r--   1 sticks sticks   1095 Oct  1 21:54  202210152029-youtube_rss_feed_prexfixs.md
-rw-rw-r--   1 sticks sticks   2154 Oct  1 21:54  202210241417-common_vim_tasks.md
-rw-rw-r--   1 sticks sticks     91 Oct  1 21:54  202211090613-post_to_archive_ph.md
-rw-rw-r--   1 sticks sticks    518 Oct  1 21:54  202212202114-war_thunder_economics.md
-rw-rw-r--   1 sticks sticks    731 Oct  1 21:54  202212291352-aukey_tp21_controls.md
-rw-rw-r--   1 sticks sticks    899 Oct  1 21:54  202301032353-notifications_to_file.md
-rw-rw-r--   1 sticks sticks     89 Oct  1 21:54  202301032358-install_notify_send.md
-rw-rw-r--   1 sticks sticks    358 Oct  1 21:54  202301312005-fd_sorted_file_list.md
-rw-rw-r--   1 sticks sticks    170 Oct  1 21:54  202302092213-youtube_urls.md
-rw-rw-r--   1 sticks sticks    212 Oct  1 21:54  20230214085636-Air_Fried_Pork_Chop.md
-rw-rw-r--   1 sticks sticks    931 Oct  1 21:54  202302141422-unbiased_chatgpt.md
-rw-rw-r--   1 sticks sticks   7757 Oct  1 21:54  202302162154-surfkeysmd.md
-rw-rw-r--   1 sticks sticks    145 Oct  1 21:54  202302191547-remove_multiple_spaces_in_vim.md
-rw-rw-r--   1 sticks sticks    273 Oct  1 21:54  202302240009-ting_recovery_codes.md
-rw-rw-r--   1 sticks sticks    391 Oct  1 21:54  202303101011-start_docker_container_at_boot.md
-rw-rw-r--   1 sticks sticks   1828 Oct  1 21:54  202303161055-vivaldi_pwa.md
-rw-rw-r--   1 sticks sticks     63 Oct  1 21:54  202303181156-thunderbird_keybindings.md
-rw-rw-r--   1 sticks sticks    115 Oct  1 21:54  202303230954-wt-invite_link_.md
-rw-rw-r--   1 sticks sticks    282 Oct  1 21:54  202303232156-open_urls_in_indivual_tabs.md
-rw-rw-r--   1 sticks sticks     66 Oct  1 21:54  202303272217-move_to_workspace_keybinds.md
-rw-rw-r--   1 sticks sticks    183 Oct  1 21:54  202303302305-set_default_browser_to_flatpak.md
-rw-rw-r--   1 sticks sticks    221 Oct  1 21:54  202304012218-x11-wayland_toggle.md
-rw-rw-r--   1 sticks sticks    146 Oct  1 21:54  202304140910-rust_notes.md
-rw-rw-r--   1 sticks sticks   2045 Oct  1 21:54  202304181610-bash_expansion_modifiers.md
-rw-rw-r--   1 sticks sticks    349 Oct  1 21:54  202304191653-pork_chop_rub.md
-rw-rw-r--   1 sticks sticks     60 Oct  1 21:54  202304241632-replace_ctrl_m_space.md
-rw-rw-r--   1 sticks sticks    151 Oct  1 21:54  202305011500-war_thunder_tournament_links.md
-rw-rw-r--   1 sticks sticks    489 Oct  1 21:54  202305152300-keyboard_as_keystrokes.md
-rw-rw-r--   1 sticks sticks    630 Oct  1 21:54  202305171441-vim_indenting.md
-rw-rw-r--   1 sticks sticks     52 Oct  1 21:54  202305311506-temp.md
-rw-rw-r--   1 sticks sticks 607430 Oct  1 21:54  202306040249-Adventures_Of_Sherlock_Holmes.md
-rw-rw-r--   1 sticks sticks     82 Oct  1 21:54  202306061955-kidspc_wifi_card_interface.md
-rw-rw-r--   1 sticks sticks   1780 Oct  1 21:54  202306160421-gnome_gsettings.md
-rw-rw-r--   1 sticks sticks    187 Oct  1 21:54  202306271317-pastebin_from_commandline.md
-rw-rw-r--   1 sticks sticks    728 Oct  1 21:54  202307021536-move_to_workspace.md
-rw-rw-r--   1 sticks sticks    304 Oct  1 21:54  202307022153-start_user_systemd_service_timers.md
-rw-rw-r--   1 sticks sticks   1118 Oct  1 21:54  202307141740-WT-Spectator-keybinds.md
-rw-rw-r--   1 sticks sticks   1391 Oct  1 21:54  202308191836-baked_pork_chops.md
-rw-rw-r--   1 sticks sticks    124 Oct  1 21:54  202308231323-docker_hub_login.md
-rw-rw-r--   1 sticks sticks    182 Oct  1 21:54  202308301115-ninja_oven_desc.md
-rw-rw-r--   1 sticks sticks   8149 Oct  1 21:54  202309031123-old_initnvim.md
-rw-rw-r--   1 sticks sticks    157 Oct  1 21:54  202309292308-pour_over_coffee_ratio.md
-rw-rw-r--   1 sticks sticks    103 Oct  1 21:54  202310021757-combine_pdf_.md
-rw-rw-r--   1 sticks sticks      0 Oct  1 21:54  202310031314-twitter_keyboard.md
-rw-rw-r--   1 sticks sticks    335 Oct  1 21:54  202310051543-extract_lines_to_file.md
-rw-rw-r--   1 sticks sticks     56 Oct  1 21:54  202310062038-james_bond_films.md
-rw-rw-r--   1 sticks sticks    248 Oct  1 21:54  202310081420-stable_difusion.md
-rw-rw-r--   1 sticks sticks    708 Oct  1 21:54  202310200301-Meatloaf_Stuffed_Peppers_with_Rice.md
-rw-rw-r--   1 sticks sticks   1597 Oct  1 21:54  202310201933-Vivaldi_command_line_switches.md
-rw-rw-r--   1 sticks sticks    163 Oct  1 21:54  202310201935-Append_the_current_line_in_vim.md
-rw-rw-r--   1 sticks sticks     50 Oct  1 21:54  202310201936-Mom_and_Pat_s_100_presidents_Cruise_in_Germany.md
-rw-rw-r--   1 sticks sticks    273 Oct  1 21:54  202310201937-Rippaverse.md
-rw-rw-r--   1 sticks sticks  25323 Oct  1 21:54  202310201938-vim_keys.md
-rw-rw-r--   1 sticks sticks     76 Oct  1 21:54  202310211609-proton_recovery_phrase.md
-rw-rw-r--   1 sticks sticks   1478 Oct  1 21:54  202310220451-Tank_Drop_Technique.md
-rw-rw-r--   1 sticks sticks   1389 Oct  1 21:54  202310230728-How_do_I_make_Sonic-Drivein_bacon_breakfast_toasters_at_home.md
-rw-rw-r--   1 sticks sticks     80 Oct  1 21:54  202310240440-wingaling_discount.md
-rw-rw-r--   1 sticks sticks    333 Oct  1 21:54  202310280214-gaijin_sale.md
-rw-rw-r--   1 sticks sticks    176 Oct  1 21:54  202312232311-twitter_webhook.md
-rw-rw-r--   1 sticks sticks    194 Oct  1 21:54  202402202352-hash_tag_collection.md
-rw-rw-r--   1 sticks sticks   1297 Oct  1 21:54  202404142316-zets-git.md
-rw-rw-r--   1 sticks sticks   1287 Oct  1 21:54  202404151817-untitled.md
-rw-rw-r--   1 sticks sticks    199 Oct  1 21:54  202405071654-change_default_file_manage_popos.md
-rw-rw-r--   1 sticks sticks    146 Oct  1 21:54  202407110922-camera_rtsp.md
-rw-rw-r--   1 sticks sticks   1703 Oct  1 21:54  202408131627-obs_default_keybinds.md
-rw-rw-r--   1 sticks sticks   3306 Oct  1 21:54  202506230810-How_to_Restart_Network_Manager_in_Ubuntu.md
-rw-rw-r--   1 sticks sticks    775 Oct  1 21:54  202506230813-mark_discord_read.md
-rw-rw-r--   1 sticks sticks   1608 Oct  1 21:54  202506230814-nvim-treesitter-markdown-fix.md
-rw-rw-r--   1 sticks sticks   2062 Oct  1 21:54  202506230816-Tell_me_about_Global_Soccer_Ventures.md
-rw-rw-r--   1 sticks sticks   1575 Oct  1 21:54  202506230830-zets_workflow.md
-rw-rw-r--   1 sticks sticks    559 Oct  1 21:54  202506230831_zets_workflow_usage.md
-rw-rw-r--   1 sticks sticks   6075 Oct  1 21:54  202506231259-tarot_cards_meanings.md
-rw-rw-r--   1 sticks sticks    643 Oct  1 21:54  202506231341-Latenight.ai.md
-rw-rw-r--   1 sticks sticks   1901 Oct  1 21:54  202506261113-Streamers_List.md
-rw-rw-r--   1 sticks sticks  11776 Oct  1 21:54  202506261301-victorian_era_roleplay_conversation.md
-rw-rw-r--   1 sticks sticks    612 Oct  1 21:54  202506301052-document10_dxcyber25.md
-rw-rw-r--   1 sticks sticks   2059 Oct  4 22:23  202510050227-document10_#dxphonk25.md
-rw-rw-r--   1 sticks sticks   1088 Oct  4 22:23  202510050227-Fudonutsunele_#WRB25.md
-rw-rw-r--   1 sticks sticks   1821 Oct  4 22:23  202510050227-late_night_ai_art_#lnaiart_oct.md
-rw-rw-r--   1 sticks sticks    594 Oct  4 22:23  202510050227-lory_ai_art_#loryaiart.md
-rw-rw-r--   1 sticks sticks    882 Oct  4 22:23  202510050227-tricia_danby_aiart_#spookhuectober25.md
-rw-rw-r--   1 sticks sticks    399 Oct  4 22:22  202510050227-yippee_ai_yay_#YIPPEELETTERW-Oct_2025.md
-rw-rw-r--   1 sticks sticks      0 Oct  9 01:17  errors.md
drwxrwxr-x   8 sticks sticks   4096 Oct  9 01:16  .git
-rw-rw-r--   1 sticks sticks  12841 Oct  9 00:51  Home.md
-rw-rw-r--   1 sticks sticks  21821 Oct  1 21:54  index.md.backup
-rw-r--r--   1 sticks sticks  17969 Oct  6 03:06 'Launching Discord.md'
-rw-rw-r--   1 sticks sticks    699 Oct  1 21:54  Scratchpad.md
-rw-rw-r--   1 sticks sticks   3143 Oct  1 21:54  Stuff.md
-rw-rw-r--   1 sticks sticks    948 Oct  1 21:54  Telescope.md
```

Now I can see what's happening. You have:
1. A `zets` directory with a `.git` folder (main repository)
2. A `zetswiki` directory with a `.git` folder (wiki repository)

The error you showed is for a **wiki** repository, not the main repository. Let me check the git remotes for both to understand better:

**Command Executed:**
```bash
cd zets && git remote -v
```

**Output:**
```
origin	git@bitbucket.org:gimpysticks/zets.git (fetch)
origin	git@bitbucket.org:gimpysticks/zets.git (push)
```


**Command Executed:**
```bash
cd zetswiki && git remote -v
```

**Output:**
```
cd: no such file or directory: zetswiki
```

Let me go back to home directory and check:

**Command Executed:**
```bash
cd /home/sticks/zetswiki && git remote -v
```

**Output:**
```
origin	https://gimpysticks@bitbucket.org/gimpysticks/zets.git/wiki (fetch)
origin	https://gimpysticks@bitbucket.org/gimpysticks/zets.git/wiki (push)
```

Perfect! Now I understand the issue. You have:

1. **Main repository** (`zets`): Uses SSH (`git@bitbucket.org:gimpysticks/zets.git`)
2. **Wiki repository** (`zetswiki`): Uses HTTPS (`https://gimpysticks@bitbucket.org/gimpysticks/zets.git/wiki`)

The authentication error is happening because:
1. **Bitbucket wikis often have different access permissions** than the main repository
2. **You're using HTTPS authentication** for the wiki, which requires your Bitbucket password
3. **The wiki might not exist or be accessible**

Here are your options to fix this:

## Option 1: Change Wiki Remote to SSH (Recommended)

**Command Executed:**
```bash
cd /home/sticks/zetswiki && git remote set-url origin git@bitbucket.org:gimpysticks/zets.git/wiki
```

**Output:**
```

```

Now let's test if the SSH connection works:

**Command Executed:**
```bash
cd /home/sticks/zetswiki && git fetch
```

**Output:**
```

```

Great! The SSH connection works. Now let's try to push:

**Command Executed:**
```bash
cd /home/sticks/zetswiki && git status
```

**Output:**
```
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	errors.md

nothing added to commit but untracked files present (use "git add" to track)
```

Perfect! Now let's try pushing:

**Command Executed:**
```bash
cd /home/sticks/zetswiki && git push
```

**Output:**
```
Enumerating objects: 193, done.
Counting objects: 100% (193/193), done.
Delta compression using up to 12 threads
Compressing objects: 100% (190/190), done.
Writing objects: 100% (191/191), 345.47 KiB | 6.64 MiB/s, done.
Total 191 (delta 0), reused 0 (delta 0), pack-reused 0
To bitbucket.org:gimpysticks/zets.git/wiki
   114e317..194a457  master -> master
```

Excellent! 🎉 The issue has been resolved! Here's what happened and what I did:

## Problem Summary
- Your **wiki repository** (`zetswiki`) was configured to use HTTPS authentication
- Bitbucket was rejecting your credentials, likely due to:
  - Account permissions on the wiki
  - Different authentication requirements for wikis
  - Possible issues with the wiki's existence or access rights

## Solution Applied
I changed your wiki repository's remote URL from HTTPS to SSH:
- **Before**: `https://gimpysticks@bitbucket.org/gimpysticks/zets.git/wiki`
- **After**: `git@bitbucket.org:gimpysticks/zets.git/wiki`

## Results
✅ **Push successful**: 191 objects pushed to the wiki repository
✅ **No authentication errors**
✅ **Using same SSH key as your main repository**

## Additional Options (if needed)
If you encounter any issues in the future, here are alternative approaches:

**Option 2: Check Wiki Access**
```bash
# Check if the wiki exists on Bitbucket's web interface
# Visit: https://bitbucket.org/gimpysticks/zets/wiki/
```
**Option 3: Regenerate App Password (for HTTPS)**
If you prefer HTTPS, create a new app password in Bitbucket:
1. Go to Bitbucket Settings → App passwords
2. Create new app password with repository permissions
3. Use that password instead of your account password

**Option 4: Use Git Credential Helper**
```bash
git config --global credential.helper store
```
Your wiki repository is now successfully synchronized with Bitbucket using SSH authentication, which matches your main repository configuration.
