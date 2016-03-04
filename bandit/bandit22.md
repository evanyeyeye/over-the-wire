# Bandit 22

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

**Solution**

```
bandit21@melinda:~$ cd /etc/cron.d
bandit21@melinda:/etc/cron.d$ ls
behemoth4_cleanup      leviathan5_cleanup     natas25_cleanup~  semtex0-ppc
cron-apt               manpage3_resetpw_job   natas26_cleanup   semtex5
cronjob_bandit22       melinda-stats          natas27_cleanup   sysstat
cronjob_bandit23       natas-session-toucher  php5              vortex0
cronjob_bandit24       natas-stats            semtex0-32        vortex20
cronjob_bandit24_root  natas25_cleanup        semtex0-64
bandit21@melinda:/etc/cron.d$ cat cronjob_bandit22
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@melinda:/etc/cron.d$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@melinda:/etc/cron.d$ file /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
/tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv: ASCII text
bandit21@melinda:/etc/cron.d$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
```

Password is Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI

*All descriptions are borrowed from OverTheWire.*
