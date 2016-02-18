# Bandit 19

The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH. 

**Solution**

```
$ ssh -t bandit18@bandit.labs.overthewire.org /bin/sh
$ echo You may also use /bin/dash or "bash --noprofile --norc" at the end of the ssh command.
You may also use /bin/dash or bash --noprofile --norc at the end of the ssh command.
$ ls
readme
$ cat readme
IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
```

Password is IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

*All descriptions are borrowed from OverTheWire.*
