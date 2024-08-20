pass :- 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

Password is stored in data.txt in rot13 form

So

cat data.txt

and we get

Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4

To decode from rot13 (you can also encode again to get the ans as f(f(x))=x)

I used tr cmd

tr '[A-Za-z]' '[N-ZA-Mn-za-m]' <<< “Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4”

And decoded it

And got the answer

The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

And there we go.