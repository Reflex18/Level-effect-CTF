# Haystack

## Description

The flag is in here somewhere...

## Files

* [haystack.zip](files/haystack.zip)

# Method

I first unziped the file and checked one of the flag readme

This provided a hexademical that converted to base64 then into this is not a flag

I then realised that the few i checked were all the same.

So i setup a grep line to find anything that wasnt the same.

this then lead to the right txt file and the flag.

grep -vr "62 47 56 32 5a 57 78 6c 5a 6d 5a 6c 59 33 52 37 5a 6d 46 72 5a 56 39 6d 62 47 46 6e 66 51 3d 3d" haystack

flag37.txt

62 47 56 32 5a 57 78 6c 5a 6d 5a 6c 59 33 52 37 63 6a 4e 6e 4d 33 68 66 5a 6e 52 33 66 51 3d 3d

I put it into cyber chef and got the flag

leveleffect{r3g3x_ftw}
