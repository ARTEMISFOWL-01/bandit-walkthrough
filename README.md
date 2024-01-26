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
ope this directory and open this file with escape character because file name is -file2<br>
password:" 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 " <br>
now login as bandit6 using this password.<br>

## level 6-7 <br>
