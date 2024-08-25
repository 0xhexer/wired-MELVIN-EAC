
Pass: - EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

THIS LEVEL CHALLENGE IS AS GOES 

The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

first man paged the given commands 
those that dosn't have a man page => go to wiki

there under the feature's section there listed the port scan 

gone to its official docs 

learned how to do a basic port scan 

Did a port scan 
got 5 ports that were actually working 
out of which 2 did not echo the text given to them (31518,31790)(when used with nc localhost <port>)

checked which one is the correct one out of the two using
openssl s_client -connect localhost:<port>

got that port 31518 is also echoing 

then checked port 31790

now that is where the problem comes 

when i pass the key to the current level(kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx) to
it  returns 

KEYUPDATE 

and when i pass something else 
it returns

wrong! please enter correct current password

Now , for this i had to seek pointers from seniors at bi0s 

and he pointed for me to learn about ncat , so did
and using the command 

nc -C -ssl localhost  31790


and boy , oh boy it worked like a charm 
and finally got the the rsa private key to the next level 


used that key in the same way as the lvl13 bandit and logged into the next level and then proceeded to get te key from /etc/bandit_pass/bandit17

there it is , the pass EReVavePLFHtFlFsjn3hyzMlvSuSAcRD


finally!!
