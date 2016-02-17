# Bandit 15

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

For this level, we will also refer to a line in the previous level's description:

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. 

**Solution**

```
bandit14@melinda:~$ cat /etc/bandit_pass/bandit14 | nc localhost 30000
Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr
```

Password is 

*All descriptions are borrowed from OverTheWire.*

