# Bandit 12

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

**Solution**

```
bandit11@melinda:~$ ls
data.txt
bandit11@melinda:~$ cat data.txt | tr a-zA-Z n-za-mN-ZA-M
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```

Password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

*All descriptions are borrowed from OverTheWire.*
