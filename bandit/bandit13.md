# Bandit 13

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!).

**Solution**

```
bandit12@melinda:~$ ls
data.txt
bandit12@melinda:~$ mkdir /tmp/evanyeyeye
bandit12@melinda:~$ cp data.txt /tmp/evanyeyeye/data.txt
bandit12@melinda:~$ cd /tmp/evanyeyeye         
bandit12@melinda:/tmp/evanyeyeye$ ls
data.txt
bandit12@melinda:/tmp/evanyeyeye$ file data.txt 
data.txt: ASCII text
bandit12@melinda:/tmp/evanyeyeye$ xxd -r data.txt > data
bandit12@melinda:/tmp/evanyeyeye$ ls
data  data.txt
bandit12@melinda:/tmp/evanyeyeye$ file data
data: gzip compressed data, was "data2.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@melinda:/tmp/evanyeyeye$ rm data.txt
bandit12@melinda:/tmp/evanyeyeye$ mv data data.gz
bandit12@melinda:/tmp/evanyeyeye$ gunzip data.gz
bandit12@melinda:/tmp/evanyeyeye$ ls       
data
bandit12@melinda:/tmp/evanyeyeye$ file data
data: bzip2 compressed data, block size = 900k
bandit12@melinda:/tmp/evanyeyeye$ bunzip2 data
bunzip2: Can't guess original name for data -- using data.out
bandit12@melinda:/tmp/evanyeyeye$ ls
data.out
bandit12@melinda:/tmp/evanyeyeye$ file data.out 
data.out: gzip compressed data, was "data4.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@melinda:/tmp/evanyeyeye$ mv data.out data.gz
bandit12@melinda:/tmp/evanyeyeye$ gunzip data.gz
bandit12@melinda:/tmp/evanyeyeye$ ls
data
bandit12@melinda:/tmp/evanyeyeye$ file data
data: POSIX tar archive (GNU)
bandit12@melinda:/tmp/evanyeyeye$ tar xvf data
data5.bin
bandit12@melinda:/tmp/evanyeyeye$ rm data
bandit12@melinda:/tmp/evanyeyeye$ file data5.bin 
data5.bin: POSIX tar archive (GNU)
bandit12@melinda:/tmp/evanyeyeye$ tar xvf data5.bin
data6.bin
bandit12@melinda:/tmp/evanyeyeye$ rm data5.bin
bandit12@melinda:/tmp/evanyeyeye$ file data6.bin 
data6.bin: bzip2 compressed data, block size = 900k
bandit12@melinda:/tmp/evanyeyeye$ bunzip2 data6.bin
bunzip2: Can't guess original name for data6.bin -- using data6.bin.out
bandit12@melinda:/tmp/evanyeyeye$ file data6.bin.out
data6.bin.out: POSIX tar archive (GNU)
bandit12@melinda:/tmp/evanyeyeye$ tar xvf data6.bin.out
data8.bin
bandit12@melinda:/tmp/evanyeyeye$ rm data6.bin.out 
bandit12@melinda:/tmp/evanyeyeye$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression
bandit12@melinda:/tmp/evanyeyeye$ mv data8.bin data.gz
bandit12@melinda:/tmp/evanyeyeye$ gunzip data.gz
bandit12@melinda:/tmp/evanyeyeye$ ls
data
bandit12@melinda:/tmp/evanyeyeye$ file data
data: ASCII text
bandit12@melinda:/tmp/evanyeyeye$ cat data
The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL
```

Password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

*All descriptions are borrowed from OverTheWire.*
