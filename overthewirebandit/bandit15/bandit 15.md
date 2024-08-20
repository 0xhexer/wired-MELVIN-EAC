
Pass: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

It is said that

“The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL/TLS encryption.”

OPENSSL seems too similar use man openssl

There was a connect option in the man page so I searched google to look how to connect to a server using ssl , and I found this

openssl s_client -connect <host>:<port>

And that’s what I did

Used the cmd

openssl s_client -connect localhost:30001

and entered the pass for the current level : 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

and got the pass
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
for next level


