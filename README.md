# Bandit-Walkthrough --Abhay

## level 0<br>

<p>we were required to access the server of bandit with username as bandit0 with port 2220 and password bandit0
hostname is bandit.labs.overthewire.org <br>
it can be done by using command <br>
" ssh bandit0@bandit.labs.overthewire.org -p 2220
password bandit0 "<br>
ssh= command to remotely access a server <br>.

## level 0-1<br>

<p>The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.<br>
use "ls" for seeing files in home directory and then use "cat readme" to get the password in this file and copy it. To logout use "exit".now do the login as same as in level 0 but with username as bandit1 and the password we got that is "NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL"<br>

## level 1-2<br>

<p>The password for the next level is stored in a file called - located in the home directory. After logging in we are in home directory to get content of the file - we cant got directoly because it wil think file name as option so we will use escape character that is ./<br>
so the command is "cat ./-"<br>
and the password we got is "rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi"<br>
after this logout using "exit" and login as bandit2 eith this password.<br>

## level 2-3<br>

The password for the next level is stored in a file called spaces in this filename located in the home directory.
to acces the file that has spaces in between we will store the file name inside "" marks.<br>
so cat "spaces in this filename".<br>
and the password we get is "aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG".now agin logout and login in as bandit3 with this password.<br>

## level 3-4<br>

The password for the next level is stored in a hidden file in the inhere directory. First change your current home directory to inhere directory by using "cd" command as "cd inhere".<br>
now to see hidden files in this directory use "ls -a", -a option will let us see hidden files.<br>
hidden file is ".hidden" now use "cat .hidden" to get password.<br>
password is "2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe", now then logout and login as bandit4 with this password.<br>

## level 4-5<br>

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.<br>
first v=change home directory to inhere directory<br>

cd inhere<br>
now there are many files in inhere but target one is human-readable so by using command to get type of all files we can find our file<br>
file ./-file\*<br>
this command will print types of all files having "file"in their name. the required file is -file07. using escape character to access it.<br>
cat ./-file07<br>
password<br>
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR<br>
now again logout and again login as bandits5 with this password.<br>

## level 5-6<br>

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:<br>

human-readable<br>
1033 bytes in size<br>
not executable<br>
First access the inhere directory with cd command, now inhere directory there are many more directories so to find required directory and file we can use find, size and type function together.<br>
"find . -type f -size 1033c"(where f is type file and c is bytes)<br>
now we get <./maybehere07/.file2><br>
ope this hidden file in the above mentioned directory, file name is .file2<br>
password:" P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU " <br>
now login as bandit6 using this password.<br>

## level 6-7 <br>

<p>The password for the next level is stored somewhere on the server and has all of the following properties:<br>

owned by user bandit7<br>
owned by group bandit6<br>
33 bytes in size<br>
for this we can use find command with user and group as option to tell ownership of file and thentype and size, but this will print some error messages to gt rid of that we will append "2>/dev/null" at the end of find command that will redirect all error mesages to dev null file <br>
"find / -user bandit7 -group bandit6 -type f -size 33c 2>/dev/null<br>"
output is "/var/lib/dpkg/info/bandit7.password"<br>
using cat command to get the content of file<br>
cat /var/lib/dpkg/info/bandit7.password<br>
password: "z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S"<br>
now logout and again login as bandit7 with this password.<br>

## level 7-8 <br>

The password for the next level is stored in the file data.txt next to the word millionth<br>
we can use "grep" command to find string containg required pattern in data.txt<br>
grep "millionth" data.txt<br>
password: "TESKZC0XvTetK0S9xNwm25STk5iWrBvP"<br>
Now again logout and login as bandit8 with this password<br>

## level 8-9<br>

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once<br>
Here we can use piping with commands sort and uniq.<br>
we will be using "-c" option with uniq to get number of lines<br>
sort data.txt | uniq -c <br>
after this we can easily find the required password for next level we can also use grep but not necessary.
pssword: "EN632PlfYiZbn3PhVK3XOGSlNInNE00t"<br>
Now again logout and login as bandit9 with this password.<br>

## level 9-10 <br>

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.<br>
we can here again use piping with "strings" and "grep" function. "strings" will see for sequence of printable characters and then we can use "grep" for finding strings with more then one = sign.<br>
strings data.txt | grep "=="<br>
password: "G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s"<br>
Now again logout and login as bandit10 with this password.<br>

## level 10-11 <br>

The password for the next level is stored in the file data.txt, which contains base64 encoded data<br>

to decrypt a base64 file we can use "base64 -d" "-d" option is use to decrypt<br>
base64 -d data.txt<br>
password: "6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM"<br>
Now again logout and login as bandit11 with this password.<br>

## level 11-12 <br>

<p>the password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.<br>

As characters are rotated by 13 positions we dont have any command to directly decrypt it so we will use "tr" command.<br>
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'<br>
A-is converted to N and so on.<br>
password: "JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv"<br>
Now again logout and login as bandit12 with this password.<br>

## level 12-13<br>

<p>The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)<br>
we will first create a directory name new in tmp and copy the data.txt there and work on it.<br>

mkdir /tmp/new<br>
cd /tmp/anew<br>
cp ~/data.txt new.txt<br>

<p>now we have a hexadump file then lets convert it to binary using xxd and storing in another place<br>

xxd -r new.txt new<br>

<p>after seeing signature of file we can apply the required unizip command.We have bzip2 and gzip now we will apply any whenever required.<br>

-mv new new.gz<br>
-gzip -d new.gz<br>
(now file is bzip2)<br>
-mv new new.bz2<br>
-bzip2 -d new.bz2<br>
(now file is gzip)<br>
-mv new new.gz<br>
-gzip -d new.gz<br>

 <p>now we will again seee signature of file but we can saw a file in its header,so to get that out of this archive we will use "tar -xf", first lets rename it.<br>

-mv new new.tar<br>
-tar -xf new.tar<br>

 <p>(now data5.bin is also a archive having data6.bin after seeing through xxd command.)<br>

-tar -xf data5.bin<br>

 <p>now data6.bin is also ziped so lets repeat the same process above.<br>
 mv data6.bin data.bz2<br>
 bzip2 -d data.bz2<br>
 xxd data<br>
 <p>now by using xxd command we found that data also has daat8.bin file so unziping this archive.<br>

tar -xf data<br>

#### decompressing data8.bin<br>

mv data8.bin data8.gz<br>
gzip -d data8.gz<br>
cat data8<br>
password: "wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw"
now again logout and login as bandit13<br>

## level 13-14<br>

<p>The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on<br>

we will be using "-i" option with ssh to use private key nad login to host localhost.<br>
ls<br>
sshkey.private(private key)<br>
ssh -i sshkey.private bandit14@localhost -p 2220<br>
cat /etc/bandit_pass/bandit14<br>
password: "fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq"

## level 14-15<br>

<p>The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.<br>

to write on internet we use nc command also called "netcat"<br>
nc localhost 30000<br>
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq<br>
"correct password"<br>
password: "jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt"<br>
now logout and login as bandit15 using this password.<br>

## level 15-16<br>

<p>The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…<br>
first get the password<br>
cat /etc/bandit_pass/bandit15<br>
password: "jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt"<br>
we can use "ncat" here which is newer version of nc.<br>
ncat --ssl localhost 30001<br>
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt<br>
password: "JQttfApK4SeyHwDlI9SXGR50qclOAil1"<br>
now logout and again login as bandit16<br>

## level 16-17<br>

<p>The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.<br>

lets get the password for this first<br>
cat /etc/bandit_pass/bandit16<br>
password: "JQttfApK4SeyHwDlI9SXGR50qclOAil1"<br>

now search for port that is active and speak ssl by using nmap<br>
nmap -sV localhost -p 31000-32000<br>
output<br>

<p>PORT      STATE SERVICE     VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo
portal 31790 is right portal as its service is unknown and speak in ssl(port 31518 service is echo,not what we want),now using ncat for writing.<br>
ncat --ssl localhost 31790<br>
JQttfApK4SeyHwDlI9SXGR50qclOAil1<br>
correct<br>

<p>-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----<br>
<p>we got a private key we will save it as a file in /tmp with some new permissions to read only by user not by public.<br>
cd / tmp<br>
vim key.private(writing and saving the key in text editor)<br>
changing permissions<br>
chmod 600 key.private<br>

Now again login as bandit17 using private key<br>
ssh -i key.private bandit17@localhost -p 2220<br>

## level 17-18<br>

<p>There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new<br>

<p>s we already are in home directory we will use "diff" to get result line in output which has < in its starting is the line of first file<br>
<p>diff passwords.new passwords.old
42c42
< hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
---
> p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW<br>
password: "hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg"<br>
