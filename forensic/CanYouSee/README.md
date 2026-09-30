# CanYouSee
## Approach
>I satrted by using commands like strings and cat and file to identify the file was jpeg and nothing came up on the strings 

![strings](/forensic/CanYouSee/canyousee/string.png)

>i also tried zsteg tool but i got to know that the command is for olny png file and BPM images


>to get more info i tried the exiftool where i found the flag encoded in the BAse 64

## Solution

The soultin is to run the exiftool command on the jpeg file to get Flag in the attribution url .

![flag_base64](/forensic/CanYouSee/canyousee/exiftool.png)

on decoding it we get the flag

## FLag
academy{ME74D47A_HIDD3N_927183b3}

## Takeaway

Remeber to use the commands to get the info of the file using exiftool