# Bandit 10

The password for the next level is stored in the file data.txt in one of the few human-readable strings, beginning with several ‘=’ characters.

**Solution**

```
bandit9@melinda:~$ ls
data.txt
bandit9@melinda:~$ strings data.txt | grep '='
epr~F=K
7?YD=
?M=HqAH
/(Ne=
C=_"
I========== the6
z5Y=
`h(8=`
n\H=;
========== password
========== ism
N$=&
l/a=L)
f=C(
========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
ie)=5e
```

Password is truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

*All descriptions are borrowed from OverTheWire.*
