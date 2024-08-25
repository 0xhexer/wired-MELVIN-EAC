
Pass:- 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

This one is easy as long as you understand it 

for this i first typed ll
and then exec bandit20-do alone without any arguments and got 

./bandit20-do

Run a command as another user.
  Example: ./bandit20-do id

running

./bandit20-do id

got the output 

uid=11019(bandit19) gid=11019(bandit19) euid=11020(bandit20) groups=11019(bandit19)

This meant that the bandit20-do can run a command as another user in this case the id command can run with an effective user id of bandit20
(have researched about  setuid bit  )

so i ran the cat command with the elf exec

./bandit20-do cat /etc/bandit_pass/bandit20 

and there you go 
we get the pass 

0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO