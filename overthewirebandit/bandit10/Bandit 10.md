pass:- dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr


This was easy

Pass stored in data.txt in base64

So doing

cat data.txt

Got me this

VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==


 Then I decoded the base 64 by

base64 -d  <<< VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==

(-d means decode , <<< for redirection as base64 on accepts files as argument by default)

And we got

The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

Yay!!

You can also do this shorter by

cat data.txt | base64 -d