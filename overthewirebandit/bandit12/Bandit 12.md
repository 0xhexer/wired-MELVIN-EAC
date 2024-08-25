
Pass:- FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

Sooo this was a long one

It was not difficult to understand (except for the little hiccup at the beginning )

but just loooong

so I will just add the screenshots

and try explain my process rather than each step

First tried use cat

Then I see that it is an hexdump stored as a text file

So have to reverse that using

xxd -r data.txt

(I have then created my temp dir in /tmp as _s_  and stored it there)

Then used file command to see what I am  working with

What comes next is an alternating compression of gzip bzip and tar few times at the end

So I used file to see wht sort of compression is it and the proceeded to decompress it accordingly

gzip -d <file> (for gzip I also changed the suffix with mv command )

bzip2 -d <file>

tar -xvf <file>

AND THERE YOU HAVE IT

The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
