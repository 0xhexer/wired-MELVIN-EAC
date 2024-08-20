Pass -morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

I was stuck on this for quite a while 
First I did cd / to change cwd to home dir then tried using (because in the question find the file from the whole server)


 find  -type f -user bandit7 -group bandit6 -size 33c

but the output contained a lot of errors,  so yea I at this point I doubting if I have done correctly 

and what is going wrong , so i searched how to solve the issue 

and what I got was this command 


find / -type f -user bandit7 -group bandit6 -size 33c 2> /dev/null


sooo , “2> /dev/null” was the missing part in my cmd 
and I dunno what that means 
I do know > is used for redirection of output to a file 


Bit of googling later , found that dev is the dir for the physical addr of devices as files (everything is a file in unix systems , known that for ages, nothing new there) 
The null part that is new though
It is a file that shreds everything that enters it .
I seeeeeeee


Then onto 2> part then 

What I learned (or rather understood ) was that the terminal has two output streams standard error (stderr, one used to output errors ) and standard output (stdout, one used by system to output everything other than stderr ) 
And the number in front of > selects which output stream to pass onto /dev/null 


Stderr is number 2
Stdout is number 1


So find  finds all files with given conditions 2> passes all the the permission error statements to /dev/null and destroys it while stdout is displayed 

And there it is the password 
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
