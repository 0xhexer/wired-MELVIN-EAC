
Pass :- EeoULMCra2q0dSkYj561DX7s1CpBuOBt

So this was kinda fun to do and also was a little tricky at the start too

So there is an elf exec that when run with port argument passed to it it will connect to that port on the localhost and reads what that port sends back

If what is sent back is the current pass 
Then it reads the pass from etc/bandit_pass(i tried gdb on it to dissamble it into but gave an error , the other thing i tried on it was doing cat on it and the human readable has the path to pass in it as opposed to the password) and print it to us 

first I used Nmap with -p argument to scan the ports

Nad I got two ports to return the password  of the current level 
8080,10300

But when I passed this to subconnect it says password correct and sending next pass 
But you never get the password 

I have no idea 
No idea at all is there some invisible character that gets sent along dunno 


Brainstormed about it thought some solution 
Finally finally an idea clicked why do you even need an already existing port when you can dedicate a port you want relay the message you want 

The googled it on how to do just that 
**
echo <prev pass> | netcat -lp <port you want to assign>
But it runs on terminal 
Means nowhere to type 
Do something  about running the ask in the background 

Goggled about it 

Finally settled on the following  cmd
echo <prev pass> | netcat -lp <port you want to assign> &

Then used subconnect with the port number used 

The Finally got the answer

EeoULMCra2q0dSkYj561DX7s1CpBuOBt

Prev pass -0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO