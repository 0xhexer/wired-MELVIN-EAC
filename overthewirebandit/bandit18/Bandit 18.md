
Pass: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

Done some research

First googled bashrc automatically logging out the user in ssh

I got the this in the form

[https://superuser.com/questions/1277825/ssh-automatically-logging-out](https://superuser.com/questions/1277825/ssh-automatically-logging-out)

and my first thought is  ,  this is quiet similar

so I sarched the web about -t option in ssh

gone to man page

which resulted in me learning about some pseudo terminal stuff

and finally I used the command

ssh [bandit18@bandit.labs.overthewire.org](mailto:bandit18@bandit.labs.overthewire.org) -t “bash --norc”

which I say tells the server to no run .bashrc when connecting to server

and since .bashrc is the file that keeps us from logging in we can finnaly log in

then used

cat readme.txt

and finally got the pass

cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

