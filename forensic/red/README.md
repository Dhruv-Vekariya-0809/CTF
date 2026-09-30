# ***RED***
## Approach
>First i tried to edit the file and see if there is anything hiddhen in the png itself  

![edit_image](forensic/red/RED/edit.png)

***

>Then I tried to use some basic commands like Strings and cat on the png file   
>It gave me a poem 

![strings](forensic/red/RED/strings.png)

> Seeing the strings in the poem i found that the first letter of the poem had highlighted letter which read <mark>Check LSB</mark>

***
I googled on how to check the LSB and i got to know of a tool called zsteg  
I installed it onto my system and got the lsb which was the flag in base 64

## Solution

for the solution you have to use a command zsteg to get the lsb   

![zsteg](forensic/red/RED/lsb.png)

the flag is hidden in the lsb of the png file. it is encoded in Base 64 so on reversing the encryption we got the flag

![flag_base64](forensic/red/RED/base64.png)

## Flag 
academy{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}

## Takeaway
learnt a new command zsteg to reveal more info on png files