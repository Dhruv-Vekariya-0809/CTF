# Transformation

## Approach

>I used commands like file, exiftool and cat to see what the file is and what it reads. it was txt file which was in UTF-8 format.  

![basic](/Rev/Transformation/transformation/basic.png)

i didnt know why was it reading chinese characters to so i googled it and found out that it happens when a text encoded UTF-16 is run as a UTF-8 encoded text and is called <mark>mojibake</mark>

![google](/Rev/Transformation/transformation/google.png)

> i searched for a command to read the UTF-8 file as UTF-16 file and found one <mark>iconv</mark>.But when i tried it it didnt gave the accurate flag.I dont know the reason.

![iconv](/Rev/Trnaformation/transformation/iconv.png)

>so then i just searched on google for a converter which gave me hex which i convertd to readable text which was the flag.

## Solution

First go the [UTF-8 to UTF-16 converter](https://onlinetools.com/utf8/convert-utf8-to-utf16) site. 

convert the file and you will get the hex string which needs to be converted to readable text .this can be done by this [site](https://www.duplichecker.com/hex-to-text.php)

you will get the flag string after doing this

## Flag

academy{16_bits_inst34d_of_8_790ba37e}

## Takeaway

using utf converter to fix the mojibake error
