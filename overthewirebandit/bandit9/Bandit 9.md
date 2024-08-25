


This has the condition password human readable preceded by SEVERAL “=”

First I tried cat data.txt | grep ==

(why == because it is given several = , so more than 1)

But I got this

grep: (standard input): binary file matches

not really error ,  but what is this

quick googling shows

 grep by default does not like to output binary data (as outputting binary data may well mess up the terminal, for instance) and therefore it defaults to just indicating a match saying binary file matches for binary files. If you want the output anyway, you may want the -a option

and I was like ok

cat data.txt | grep -a ==

I spotted the pass

But I have not really implemented the human readable condition so lets use strings instead cat

Final cmd

Strings data.txt | grep -a ==

And we got


Pass = FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

