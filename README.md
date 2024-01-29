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
