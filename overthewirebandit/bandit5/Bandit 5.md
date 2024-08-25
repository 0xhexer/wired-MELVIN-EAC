Pass : - HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

did 
find ./* -size 1033c | xargs file | grep ASCII

did not use the not exec in find 
then again whstever is ASCII is not exec
xargs allows the output of find as an argument for file

output of that is 
./inhere/maybehere07/.file2: ASCII text, with very long lines (1000)

then used 

cat ./inhere/maybehere07/.file2
and got the pass

HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
