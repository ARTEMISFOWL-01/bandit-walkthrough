 #Bandit-Walkthrough --Abhay 

##level 0<br>

<p>we were required to access the server of bandit with username as bandit0 with port 2220 and password bandit0
hostname is bandit.labs.overthewire.org <br>
it can be done by using command <br>
"ssh bandit0@bandit.labs.overthewire.org -p 2220
password bandit0" <br>
ssh= command to remotely access a server <br.

##level 0-1<br>
<p>The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.<br>
use "ls" for seeing files in home directory and then use "cat readme" to get the password in this file and copy it. To exit logout use "exit".<br>


