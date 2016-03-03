# Bandit 20

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used to setuid binary.

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
