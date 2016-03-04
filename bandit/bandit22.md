# Bandit 22

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

**Solution**

```
bandit19@melinda:~$ ls
bandit20-do
bandit19@melinda:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
bandit19@melinda:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```

Password is GbKksEFF4yrVs6il55v6gwY5aVje5f0j

*All descriptions are borrowed from OverTheWire.*
