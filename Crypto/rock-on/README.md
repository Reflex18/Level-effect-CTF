# Rock on

## Description

Getting it out is the easy part, but good luck getting in.

## Files

* [capture.pcap](files/capture.pcap)

# Method:

We were presented with a pcap file and i opened it up using wireshark to get a better look at it.

Within this file there are only 26 packets so its quite small and easy enought to look at without extensive filters.

First i checked if there was any files that wireshark could carve out of it.

You can do this by going files>export objects>http data

This opens up a window that shows what data wireshark found within the packets.

Something is rather interesting here and that is the flag.zip file. Time to download that.

Getting the zip file was indeed rather easy, lets unzip it and find out whats inside.

Well the zip file needs a password... how do we crack it and get inside?

To do this i used a tool called fcrackzip with the following tags

`fcrackzip -v -D -u -p rockyou.txt flag.zip`

-v :This is for verbose to show more info
-D :this is to use a dictionary attack
-u :this is to tell it to attempt to unzip it to show what are the wrong passwords
-p :This tag is to print out the password found.

I also used the rockyou.txt as my txt file with the list of passwords to try.

`PASSWORD FOUND!!!!: pw == Cena.John.Rulz

I tried that and opened the file to find a pdf.

This pdf was also password protected.

I looked up a pdf cracker for linux and found pdfcrack.

After installing it and using the following in the terminal i found the password.

`pdfcrack -w rockyou.txt flag.pdf

`found user-password: 'Fcrunner1337'`

Opening the file with that password got the following flag

flag = leveleffect{L367_g37_cr4ck1n}


