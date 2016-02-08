# Bandit 6

The password for the next level is stored somewhere on the server and has all of the following properties: - owned by user bandit7 - owned by group bandit6 - 33 bytes in size

**Solution**

```
bandit6@melinda:~$ ls
bandit6@melinda:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@melinda:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```

Password is HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

*All descriptions are borrowed from OverTheWire.*
