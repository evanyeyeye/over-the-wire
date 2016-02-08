# Bandit 6

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties: - human-readable - 1033 bytes in size - not executable

**Solution**

```
bandit5@melinda:~$ ls 
inhere
bandit5@melinda:~$ ls inhere
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@melinda:~$ find inhere -readable -size 1033c ! -executable
inhere/maybehere07/.file2
bandit5@melinda:~$ cat inhere/maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```

Password is DXjZPULLxYr17uwoI01bNLQbtFemEgo7

*All descriptions are borrowed from OverTheWire.*
