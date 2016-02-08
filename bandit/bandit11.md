# Bandit 11

The password for the next level is stored in the file data.txt, which contains base64 encoded data.

**Solution**

```
bandit10@melinda:~$ ls
data.txt
bandit10@melinda:~$ base64 -d data.txt 
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```

Password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

*All descriptions are borrowed from OverTheWire.*
