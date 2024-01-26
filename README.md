#Bandit-Walkthrough --Abhay

##level 0<br>

<p>we were required to access the server of bandit with username as bandit0 with port 2220 and password bandit0
hostname is bandit.labs.overthewire.org <br>
it can be done by using command <br>
 "ssh bandit0@bandit.labs.overthewire.org -p 2220
password bandit0" <br>
ssh= command to remotely access a server <br>.

##level 0-1<br>

<p>The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.<br>
use "ls" for seeing files in home directory and then use "cat readme" to get the password in this file and copy it. To logout use "exit".now do the login as same as in level 0 but with username as bandit1 and the password we got that is "NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL"<br>

##level 1-2<br>

<p>The password for the next level is stored in a file called - located in the home directory. After logging in we are in home directory to get content of the file - we cant got directoly because it wil think file name as option so we will use escape character that is ./<br>
so the command is "cat ./-"<br>
and the password we got is "rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi"<br>
after this logout using "exit" and login as bandit2 eith this password.<br>

##level 2-3<br>

The password for the next level is stored in a file called spaces in this filename located in the home directory.
to acces the file that has spaces in between we will store the file name inside "" marks.<br>
so cat "spaces in this filename".<br>
and the password we get is "aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG".now agin logout and login in as bandit3 with this password.<br>

##level 3-4<br>

The password for the next level is stored in a hidden file in the inhere directory. First change your current home directory to inhere directory by using "cd" command as "cd inhere".<br>
now to see hidden files in this directory use "ls -a", -a option will let us see hidden files.<br>
hidden file is ".hidden" now use "cat .hidden" to get password.<br>
password is "2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe", now then logout and login as bandit4 with this password.<br>

## level 4-5<br>
