# Bandit 16

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Remember that the password to access this level was BfMYroe26WYalil77FoDi9qh59eK5xNr

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

**Solution**

```
bandit15@melinda:~$ openssl s_client -connect localhost:30001 -ign_eof -quiet
depth=0 CN = li190-250.members.linode.com
verify error:num=18:self signed certificate
verify return:1
depth=0 CN = li190-250.members.linode.com
verify return:1
BfMYroe26WYalil77FoDi9qh59eK5xNr
Correct!
cluFn7wTiGryunymYOu4RcffSxQluehd
read:errno=0
```

Password is cluFn7wTiGryunymYOu4RcffSxQluehd

*All descriptions are borrowed from OverTheWire.*
