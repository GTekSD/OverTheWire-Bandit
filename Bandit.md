## Bandit Level 0

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit0@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit0@bandit.labs.overthewire.org's password: bandit0

      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

 Both python2 and python3 are installed.

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit0@bandit:~$ 

```

## Bandit Level 0 → Level 1

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
```
bandit0@bandit:~$ pwd
/home/bandit0
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme 
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```

### Bandit Level 1 → Level 2

The password for the next level is stored in a file called - located in the home directory
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit1@bandit.labs.overthewire.org -p 2220

bandit1@bandit.labs.overthewire.org's password: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

bandit1@bandit:~$ 
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/- 
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```

## Bandit Level 2 → Level 3

The password for the next level is stored in a file called spaces in this filename located in the home directory
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit2@bandit.labs.overthewire.org -p 2220

bandit2@bandit.labs.overthewire.org's password: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit2@bandit:~$ 
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename 
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```

## Bandit Level 3 → Level 4

The password for the next level is stored in a hidden file in the inhere directory.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit3@bandit.labs.overthewire.org -p 2220

bandit3@bandit.labs.overthewire.org's password: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cat inhere/.hidden 
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```

## Bandit Level 4 → Level 5

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ ls inhere/
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~$ cat inhere/-file*
 Ű  Bη   b<Q Ƞ +V iO 1 [5{ jmD B 0D tQ*  ) A   V  ]Ȕl x(  z  .T26 F8qqlY   v FN#  '~ E Q " p 
    4 } ]  G A  u[ /9  Mrj S r_E ,     G+ h| +
 =>KQ 2  ]o-p8q 츑   D 
                       .~  &ϯ"PT I' cwk^j       M    ;,   co 9lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
 ׉ǰ 6= >> ӫ w <U'= @  Z xj ?3  [ٲN|? G|b G [8 y - * 
                                                      
                                                      bandit4@bandit:~$ 
bandit4@bandit:~$ cat inhere/-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.

```

## Bandit Level 5 → Level 6

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit5@bandit.labs.overthewire.org -p 2220

bandit5@bandit.labs.overthewire.org's password: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ll
total 88
drwxr-x--- 22 root bandit5 4096 Apr 23 18:04 ./
drwxr-xr-x  3 root root    4096 Apr 23 18:04 ../
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere00/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere01/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere02/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere03/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere04/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere05/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere06/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere07/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere08/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere09/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere10/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere11/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere12/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere13/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere14/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere15/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere16/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere17/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere18/
drwxr-x---  2 root bandit5 4096 Apr 23 18:04 maybehere19/
bandit5@bandit:~/inhere$ cat maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
bandit5@bandit:~/inhere$ exit
logout
Connection to bandit.labs.overthewire.org closed.

```

## Bandit Level 6 → Level 7

The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit6@bandit.labs.overthewire.org -p 2220

bandit6@bandit.labs.overthewire.org's password: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

bandit6@bandit:~$ find / -user bandit7 -group bandit6 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
 
```

## Bandit Level 7 → Level 8

The password for the next level is stored in the file data.txt next to the word millionth
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit7@bandit.labs.overthewire.org -p 2220

bandit7@bandit.labs.overthewire.org's password: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.

```

## Bandit Level 8 → Level 9

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit8@bandit.labs.overthewire.org -p 2220

bandit8@bandit.labs.overthewire.org's password: TESKZC0XvTetK0S9xNwm25STk5iWrBvP

bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ cat data.txt | wc -l
1001
bandit8@bandit:~$ cat data.txt | sort -u | wc -l
101
bandit8@bandit:~$ cat data.txt | sort | uniq -u | wc -l
1
bandit8@bandit:~$ cat data.txt | sort | uniq -u 
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
bandit8@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
 
```

## Bandit Level 9  → Level 10

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit9@bandit.labs.overthewire.org -p 2220

bandit9@bandit.labs.overthewire.org's password: EN632PlfYiZbn3PhVK3XOGSlNInNE00t

bandit9@bandit:~$ cat data.txt | grep =
grep: (standard input): binary file matches
bandit9@bandit:~$ strings data.txt | grep =
4========== the#
5P=GnFE
========== password
'DN9=5
========== is
$Z=_
=TU%
=^,T,?
W=y 
q=W 
X=K,
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
&S=(
nd?=
bandit9@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
 
```

## Bandit Level 10 → Level 11

The password for the next level is stored in the file data.txt, which contains base64 encoded data
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit10@bandit.labs.overthewire.org -p 2220

bandit10@bandit.labs.overthewire.org's password: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ base64 -d data.txt 
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```

## Bandit Level 11 → Level 12

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit11@bandit.labs.overthewire.org -p 2220

bandit11@bandit.labs.overthewire.org's password: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.

```

## Bandit Level 12 → Level 13

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit12@bandit.labs.overthewire.org -p 2220

bandit12@bandit.labs.overthewire.org's password: JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

bandit12@bandit:~$ ll
total 24
drwxr-xr-x  2 root     root     4096 Apr 23 18:04 ./
drwxr-xr-x 70 root     root     4096 Apr 23 18:05 ../
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit13 bandit12 2642 Apr 23 18:04 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit12@bandit:~$ chmod 777 data.txt 
chmod: changing permissions of 'data.txt': Operation not permitted
bandit12@bandit:~$ mkdir /tmp/unzip_dat/
bandit12@bandit:~$ cp data.txt /tmp/unzip_dat/
bandit12@bandit:~$ cd /tmp/unzip_dat
bandit12@bandit:/tmp/unzip_dat$ ll
total 1164
drwxrwxr-x    2 bandit12 bandit12    4096 May  3 12:05 ./
drwxrwx-wt 1032 root     root     1179648 May  3 12:05 ../
-rw-r-----    1 bandit12 bandit12    2642 May  3 12:05 data.txt
bandit12@bandit:/tmp/unzip_dat$ 

bandit12@bandit:/tmp/unzip_dat$ xxd -r data.txt data_xxd
bandit12@bandit:/tmp/unzip_dat$ ls
data.txt  data_xxd
bandit12@bandit:/tmp/unzip_dat$ file data_xxd 
data_xxd: gzip compressed data, was "data2.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 581
bandit12@bandit:/tmp/unzip_dat$ mv data_xxd data.gz
bandit12@bandit:/tmp/unzip_dat$ ls
data.gz  data.txt
bandit12@bandit:/tmp/unzip_dat$ gunzip data.gz 

bandit12@bandit:/tmp/unzip_dat$ ls
data  data.txt
bandit12@bandit:/tmp/unzip_dat$ file data
data: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/unzip_dat$ mv data data.bz2
bandit12@bandit:/tmp/unzip_dat$ bzip2 -d data.bz2 

bandit12@bandit:/tmp/unzip_dat$ ls
data  data.txt
bandit12@bandit:/tmp/unzip_dat$ file data
data: gzip compressed data, was "data4.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/unzip_dat$ mv data data.gz
bandit12@bandit:/tmp/unzip_dat$ gunzip data.gz 

bandit12@bandit:/tmp/unzip_dat$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/unzip_dat$ tar -xvf data
data5.bin
bandit12@bandit:/tmp/unzip_dat$ file data5.bin 
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/unzip_dat$ tar -xvf data5.bin
data6.bin

bandit12@bandit:/tmp/unzip_dat$ file data6.bin 
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/unzip_dat$ ls
data5.bin  data6.bin  data.txt
bandit12@bandit:/tmp/unzip_dat$ tar -xvjf data6.bin
data8.bin
bandit12@bandit:/tmp/unzip_dat$ file data8.bin 
data8.bin: gzip compressed data, was "data9.bin", last modified: Sun Apr 23 18:04:23 2023, max compression, from Unix, original size modulo 2^32 49

bandit12@bandit:/tmp/unzip_dat$ mv data8.bin data8.gz
bandit12@bandit:/tmp/unzip_dat$ gunzip data8.gz 
bandit12@bandit:/tmp/unzip_dat$ ls
data5.bin  data6.bin  data8  data.txt  
bandit12@bandit:/tmp/unzip_dat$ file data8
data8: ASCII text
bandit12@bandit:/tmp/unzip_dat$ cat data8
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
bandit12@bandit:/tmp/unzip_dat$ 
bandit12@bandit:/tmp/unzip_dat$ exit
logout
Connection to bandit.labs.overthewire.org closed.
  
```

## Bandit Level 13 → Level 14

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit13@bandit.labs.overthewire.org -p 2220

bandit13@bandit.labs.overthewire.org's password: wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

bandit13@bandit:~$ cat sshkey.private 
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAxkkOE83W2cOT7IWhFc9aPaaQmQDdgzuXCv+ppZHa++buSkN+
gg0tcr7Fw8NLGa5+Uzec2rEg0WmeevB13AIoYp0MZyETq46t+jk9puNwZwIt9XgB
ZufGtZEwWbFWw/vVLNwOXBe4UWStGRWzgPpEeSv5Tb1VjLZIBdGphTIK22Amz6Zb
ThMsiMnyJafEwJ/T8PQO3myS91vUHEuoOMAzoUID4kN0MEZ3+XahyK0HJVq68KsV
ObefXG1vvA3GAJ29kxJaqvRfgYnqZryWN7w3CHjNU4c/2Jkp+n8L0SnxaNA+WYA7
jiPyTF0is8uzMlYQ4l1Lzh/8/MpvhCQF8r22dwIDAQABAoIBAQC6dWBjhyEOzjeA
J3j/RWmap9M5zfJ/wb2bfidNpwbB8rsJ4sZIDZQ7XuIh4LfygoAQSS+bBw3RXvzE
pvJt3SmU8hIDuLsCjL1VnBY5pY7Bju8g8aR/3FyjyNAqx/TLfzlLYfOu7i9Jet67
xAh0tONG/u8FB5I3LAI2Vp6OviwvdWeC4nOxCthldpuPKNLA8rmMMVRTKQ+7T2VS
nXmwYckKUcUgzoVSpiNZaS0zUDypdpy2+tRH3MQa5kqN1YKjvF8RC47woOYCktsD
o3FFpGNFec9Taa3Msy+DfQQhHKZFKIL3bJDONtmrVvtYK40/yeU4aZ/HA2DQzwhe
ol1AfiEhAoGBAOnVjosBkm7sblK+n4IEwPxs8sOmhPnTDUy5WGrpSCrXOmsVIBUf
laL3ZGLx3xCIwtCnEucB9DvN2HZkupc/h6hTKUYLqXuyLD8njTrbRhLgbC9QrKrS
M1F2fSTxVqPtZDlDMwjNR04xHA/fKh8bXXyTMqOHNJTHHNhbh3McdURjAoGBANkU
1hqfnw7+aXncJ9bjysr1ZWbqOE5Nd8AFgfwaKuGTTVX2NsUQnCMWdOp+wFak40JH
PKWkJNdBG+ex0H9JNQsTK3X5PBMAS8AfX0GrKeuwKWA6erytVTqjOfLYcdp5+z9s
8DtVCxDuVsM+i4X8UqIGOlvGbtKEVokHPFXP1q/dAoGAcHg5YX7WEehCgCYTzpO+
xysX8ScM2qS6xuZ3MqUWAxUWkh7NGZvhe0sGy9iOdANzwKw7mUUFViaCMR/t54W1
GC83sOs3D7n5Mj8x3NdO8xFit7dT9a245TvaoYQ7KgmqpSg/ScKCw4c3eiLava+J
3btnJeSIU+8ZXq9XjPRpKwUCgYA7z6LiOQKxNeXH3qHXcnHok855maUj5fJNpPbY
iDkyZ8ySF8GlcFsky8Yw6fWCqfG3zDrohJ5l9JmEsBh7SadkwsZhvecQcS9t4vby
9/8X4jS0P8ibfcKS4nBP+dT81kkkg5Z5MohXBORA7VWx+ACohcDEkprsQ+w32xeD
qT1EvQKBgQDKm8ws2ByvSUVs9GjTilCajFqLJ0eVYzRPaY6f++Gv/UVfAPV4c+S0
kAWpXbv5tbkkzbS0eaLPTKgLzavXtQoTtKwrjpolHKIHUz6Wu+n4abfAIRFubOdN
/+aLoRQ0yBDRbdXMsZN/jvY44eM+xRLdRVyMmdPtP8belRi2E2aEzA==
-----END RSA PRIVATE KEY-----
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit13/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_hosts).

Welcome to OverTheWire!

  Enjoy your stay!

bandit14@bandit:~$ 

```

## Bandit Level 14 → Level 15

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.
```
┌──(kali㉿kali)-[~]
└─$ bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220

bandit14@bandit:~$ cd /etc/bandit_pass/
bandit14@bandit:/etc/bandit_pass$ cat * 2>/dev/null
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:/etc/bandit_pass$ echo fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq | nc localhost 30000
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

bandit14@bandit:/etc/bandit_pass$ exit
logout
Connection to localhost closed.

```

## Bandit Level 15 → Level 16

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit15@bandit.labs.overthewire.org -p 2220

bandit15@bandit.labs.overthewire.org's password: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

bandit15@bandit:~$ cat /etc/bandit_pass/bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=May  2 11:40:22 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=May  2 11:40:22 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: May  2 11:39:22 2023 GMT; NotAfter: May  2 11:40:22 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEX3H5dTANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwNTAyMTEzOTIyWhcNMjMwNTAyMTE0MDIyWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDg
JP3DWzxqtK3a/ev2seQfq44iWAL6IKuJPgA0DfE5BUPZOte8Z65w1Nzb5gCyXb1p
LRD94C8yKFpAECrrBUKaURf9+JuS+Ip3Uow173XaLaUWDkQM1oCtvGuzM7aCL+ET
Mn7aT4xAhqwgQIhdqmUdTdgooVKzu+fbipCR8r3HErsfcl43B4S8yt81kwS51TNP
M7AzgZhFqm2i0DZAulz/xfp1oju7zxWUxHIqxnSaSZBm+wXISv5wMbL4LIV43FXK
2kbFbm2PYlCwioKlvuAFOEDQ+u9hFImBArcmjI363KX5Q2Rq+WutFnYS/P7FEOi5
S7tBlQpA4y9IXFOnz3WDAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQDc
7OuI8VXXyBO+iHnZJz9PowLuvsVrQtHBuLSSSALdirD0gbM2VJ5X06N1rflkc8Vx
5BQ+scidIzCR+4u1y3V6jJ1ktgHuIBVQAl4tVDMXUtO0JPO9SRb4YbpM4ZCXpPZa
I2ft6Fn+enG8VkdwGTBaJqeRiEyALM+JiMnUcCjM/YtUffNahxIsiR7iHsOZ7sVJ
OqH7Py+kMiFKOBBusFz6zQMhs+gT5b74TmytrzD0yVRhf5TKm6qGNzf9PK4PSOmj
d0V5yZJz9uBiIMmYq8otHIh1cQuQaV8uttvykOXNZiI0xzj3mxK1fyy8Ai3xtMsH
njWIzKkGS8aCB7LCXTaw
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 145E19291BD1AFA3A79F008EAF588B2C4CA9AC7F3FE3934D539E7A1C1A1892F5
    Session-ID-ctx: 
    Resumption PSK: FB6511E1D32C23F8337F54C055E25FAE9EF0F18B4EA07CDDE76E4DA52267F9FF9F7B07E142C1E3E6E6D91DD059231D70
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 2e 3b 22 05 8a 68 e0 12-ec db 3b 60 ae c9 25 02   .;"..h....;`..%.
    0010 - 05 a6 9d 73 49 b1 81 41-81 4b e8 22 7c e4 09 3c   ...sI..A.K."|..<
    0020 - cc d7 9d 31 82 32 e5 2c-95 a2 d6 b3 57 45 f2 f9   ...1.2.,....WE..
    0030 - 1b bf a8 da ab df 3e 52-b1 64 2d 4c 21 8c 04 dd   ......>R.d-L!...
    0040 - ba d3 7a 4f db c9 8c 2d-cc 07 81 90 83 86 10 c1   ..zO...-........
    0050 - a1 9d 2b ca 51 a8 00 53-80 be cf 2d d3 72 0e e5   ..+.Q..S...-.r..
    0060 - b5 ba 1e ae ad 54 19 e4-ab b2 c6 f7 8b 2e b9 19   .....T..........
    0070 - c6 c3 ce c4 6c c1 e2 0d-dd 1a e6 94 61 ef 12 80   ....l.......a...
    0080 - 6a 65 9d b1 f4 4a c5 8a-45 4e e7 b2 5a c5 e4 0c   je...J..EN..Z...
    0090 - a1 87 7c ee 73 b2 71 41-5a 4f c8 52 4f 0a 2d 04   ..|.s.qAZO.RO.-.
    00a0 - f3 37 05 95 00 c2 19 9c-3b 1b 50 d8 f3 1f ea d4   .7......;.P.....
    00b0 - 18 f1 65 0d 45 46 1d 56-12 4f f6 26 2c ae 6d 5f   ..e.EF.V.O.&,.m_
    00c0 - 97 ff 4d 64 89 4f 51 a5-6f 37 e1 cb d7 f8 09 76   ..Md.OQ.o7.....v

    Start Time: 1683119862
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: AAE5077DD7E7BE6B831C1718419C5FC2D84CC9BAA03A0A7F0BFD2ED29E4AB76F
    Session-ID-ctx: 
    Resumption PSK: 4991DD2756C119E048366C49A01F3FB7C1494822B238DA628F5E3E9BC2F883518A1FB4AC7290A789CAD330C72EE7DA7D
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 2e 3b 22 05 8a 68 e0 12-ec db 3b 60 ae c9 25 02   .;"..h....;`..%.
    0010 - ff be de eb 1a 08 1e 8b-4c 96 0b c7 b1 0b 7a 12   ........L.....z.
    0020 - 89 6a bf 24 5a f2 d7 5f-4c 01 ef e7 fc 52 dd 61   .j.$Z.._L....R.a
    0030 - d5 39 ef 0f 4a 74 87 69-3d 14 81 a6 a9 70 70 1e   .9..Jt.i=....pp.
    0040 - a2 fc 10 74 38 1f a1 ce-b8 41 ad 9a b3 b2 a1 3b   ...t8....A.....;
    0050 - 51 c0 74 da 96 74 48 e8-b8 74 ef 2b 75 24 71 7d   Q.t..tH..t.+u$q}
    0060 - d9 38 74 70 46 fd b4 95-e4 61 b6 12 04 0f 9a a8   .8tpF....a......
    0070 - db ce cb b3 8a 77 b8 20-23 11 1f ff f9 0e 08 b4   .....w. #.......
    0080 - 49 92 0d 74 a4 db ac bc-f0 b7 b7 9d 78 cf f8 fd   I..t........x...
    0090 - 52 16 85 f3 5a 1a c4 00-85 c7 7d 24 ac a7 1d 54   R...Z.....}$...T
    00a0 - f4 9b 77 0d 1c 0e bd 15-24 b1 14 dc ee a7 3c 42   ..w.....$.....<B
    00b0 - d0 41 60 8e d8 b3 91 56-6f ef 4e b4 da 37 d4 0b   .A`....Vo.N..7..
    00c0 - f3 04 c9 fd d3 d7 c7 e7-6e 20 1f 98 af f7 fc f9   ........n ......

    Start Time: 1683119862
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit15@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.
```

## Bandit Level 16 → Level 17

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit16@bandit.labs.overthewire.org -p 2220

bandit16@bandit.labs.overthewire.org's password: JQttfApK4SeyHwDlI9SXGR50qclOAil1

```

## Bandit Level 17 → Level 18

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit17@bandit.labs.overthewire.org -p 2220

bandit17@bandit.labs.overthewire.org's password: 

```

## Bandit Level 18 → Level 19

The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit18@bandit.labs.overthewire.org -p 2220

bandit18@bandit.labs.overthewire.org's password: 

```

## Bandit Level 19 → Level 20

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit19@bandit.labs.overthewire.org -p 2220

bandit19@bandit.labs.overthewire.org's password: 

```

## Bandit Level 20 → Level 21

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit20@bandit.labs.overthewire.org -p 2220

bandit20@bandit.labs.overthewire.org's password: 

```

## Bandit Level 21 → Level 22

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 22 → Level 23

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 23 → Level 24

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 24 → Level 25

A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 25 → Level 26

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 26 → Level 27

Good job getting a shell! Now hurry and grab the password for bandit27!
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 27 → Level 28

There is a git repository at ssh://bandit27-git@localhost/home/bandit27-git/repo. The password for the user bandit27-git is the same as for the user bandit27.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 28 → Level 29

There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo. The password for the user bandit28-git is the same as for the user bandit28.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 29 → Level 30

There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo. The password for the user bandit29-git is the same as for the user bandit29.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 30 → Level 31

There is a git repository at ssh://bandit30-git@localhost/home/bandit30-git/repo. The password for the user bandit30-git is the same as for the user bandit30.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 31 → Level 32

There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo. The password for the user bandit31-git is the same as for the user bandit31.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 32 → Level 33

After all this git stuff its time for another escape. Good luck!
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

## Bandit Level 33 → Level 34

At this moment, level 34 does not exist yet.
```
┌──(kali㉿kali)-[~]
└─$ ssh bandit4@bandit.labs.overthewire.org -p 2220

bandit4@bandit.labs.overthewire.org's password: 

```

