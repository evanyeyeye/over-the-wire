# Bandit 5

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

**Solution**

```
bandit4@melinda:~$ ls
inhere
bandit4@melinda:~$ file inhere/*
inhere/-file00: data
inhere/-file01: data
inhere/-file02: data
inhere/-file03: data
inhere/-file04: data
inhere/-file05: data
inhere/-file06: data
inhere/-file07: ASCII text
inhere/-file08: data
inhere/-file09: data
bandit4@melinda:~$ cat inhere/-file07
koReBOKuIDDepwhWk7jZC0RTdopnAYKh
```

Password is koReBOKuIDDepwhWk7jZC0RTdopnAYKh

*All descriptions are borrowed from OverTheWire.*
