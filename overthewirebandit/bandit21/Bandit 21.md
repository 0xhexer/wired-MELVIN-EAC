
Pass:- tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

first looking at the given challenge

"A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed"

first did 

man cron 

I got the discription 

    cron - daemon to execute scheduled commands (Vixie Cron)

i searched what a dameon is
and found that it is 

**a computer program running in the background of a multitasking operating system (OS)**

so cron is like a command to make a program run in the background at sheduled intervals 

okayyy

then  i moved onto 
the /etc/cron.d dir 
and listed all the files there 

cronjob_bandit22 cronjob_bandit23 cronjob_bandit24 e2scrub_all otw-tmp-dir sysstat 


and i think our level is pretaining level22 so i did 

cat cronjob_bandit22

and got 

@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null 
** * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null

which i think means that at reboot this bash script cronjob_bandit22.sh runs and redirects the output to null (destroy)

anyways 
gone to dir /usr/bin/cronjob_bandit22.sh to check the script 

did a cat on it and got 

#!/bin/bash 
chmod 644 /tmp/t706lds9S0RqQh9aMcz6ShpAoZKF7fgv 
cat /etc/bandit_pass/bandit22 > /tmp/t706lds9S0RqQh9aMcz6ShpAoZKF7fgv

this script first changes the permission for t706lds9S0RqQh9aMcz6ShpAoZKF7fgv in tmp
and then copies required pass to that file 

so we should be able to find our pass at /tmp/t706lds9S0RqQh9aMcz6ShpAoZKF7fgv
(something of note i found interesting the redirection to /dev/null is actually not necessary for it to run although i suppose it is there in case there is some error like file not found )

did cat /tmp/t706lds9S0RqQh9aMcz6ShpAoZKF7fgvand 

and got he required pass 
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q




