# Bandit 9

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

**Solution**

```
bandit8@melinda:~$ ls
data.txt
bandit8@melinda:~$ cat data.txt | sort | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```

Password is UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

*All descriptions are borrowed from OverTheWire.*
