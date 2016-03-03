# Bandit 21

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: To beat this level, you need to login twice: once to run the setuid command, and once to start a network daemon to which the setuid will connect.

NOTE 2: Try connecting to your own network daemon to see if it works as you think

Remember that the password to this level was GbKksEFF4yrVs6il55v6gwY5aVje5f0j.

**Solution**

*Terminal 1*
```
bandit20@melinda:~$ ls
suconnect
bandit20@melinda:~$ ./suconnect
Usage: ./suconnect <portnumber>
This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.
```

*Terminal 2*
```
bandit20@melinda:~$ nc -l -p 1234
```

*Terminal 1*
```
bandit20@melinda:~$ ./suconnect 1234
```

*Terminal 2*
```
GbKksEFF4yrVs6il55v6gwY5aVje5f0j
```

*Terminal 1*
```
Read: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
Password matches, sending next password
```

*Terminal 2*
```
gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
```

Password is gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

*All descriptions are borrowed from OverTheWire.*
