# Bandit 23

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

**Solution**

```
bandit22@melinda:~$ cd /etc/cron.d
bandit22@melinda:/etc/cron.d$ ls
behemoth4_cleanup      leviathan5_cleanup     natas25_cleanup~  semtex0-ppc
cron-apt               manpage3_resetpw_job   natas26_cleanup   semtex5
cronjob_bandit22       melinda-stats          natas27_cleanup   sysstat
cronjob_bandit23       natas-session-toucher  php5              vortex0
cronjob_bandit24       natas-stats            semtex0-32        vortex20
cronjob_bandit24_root  natas25_cleanup        semtex0-64
bandit22@melinda:/etc/cron.d$ cat cronjob_bandit23
* * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
bandit22@melinda:/etc/cron.d$ cat /usr/bin/cronjob_bandit23.sh
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
bandit22@melinda:/etc/cron.d$ echo I am user bandit23 | md5sum | cut -d ' ' -f 1
8ca319486bfbbc3663ea0fbe81326349
bandit22@melinda:/etc/cron.d$ cat /tmp/8ca319486bfbbc3663ea0fbe81326349
jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
```

Password is jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n

*All descriptions are borrowed from OverTheWire.*
