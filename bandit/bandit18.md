# Bandit 18

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

**Solution**

```
bandit17@melinda:~$ ls
passwords.new  passwords.old
bandit17@melinda:~$ diff passwords.new passwords.old
42c42
< kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
---
> BS8bqB1kqkinKJjuxL6k072Qq9NRwQpR
```

Password is kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

*All descriptions are borrowed from OverTheWire.*
