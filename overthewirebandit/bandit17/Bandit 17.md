
Pass: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

Given 2 files with  only one diff line and the diff one in password,new is the pass

Exec cmd

diff password.new password.old

bandit17@bandit:~$ diff passwords.new passwords.old

42c42

< x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
> bSrACvJvvBSxEM2SGsV5sn09vc3xgqyp

Returned the above section

< implies it came from first argument

Which implies

Password is x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO