# Bits abound

## Description

I have a key with a curious code etched into it but not a clue where it goes. Here, take a look and let me know if you discover anything even the least bit significant about it.

## Files

* [key.png](files/key.png)

# Method

First thing i did was to just read over the description of the challenge again.

This lead to me thinking that it had to do something with the least significant bit.

I then used a tool called zsteg with the parameter of -A to search for every method inside of the picture.

To install zsteg you will need to use the following: `gem install zsteg`

Tool is fro: https://github.com/zed-0xff/zsteg

After running zsteg it prints out alot of information in the terminal with the important information being red.

The following caught my eye as base64:

`TW9Xb01vR2xEaVVxVmtYVVVlfnpUfn5+VmV+a09ufn5WZX5+Tm1EfklvU3c=`

It then decodes to the following

`MoWoMoGlDiUqVkXUUe~zT~~~Ve~kOn~~Ve~~NmD~IoSw`

This made no sense to me for awhile so i had to do some research and understand what this code meant and how did it relate to the picture.

The picture is of a key with 21A on it.

I tried the vigenere cipher since it needs a key input but that did not work.

After plenty of googling and seraching up common stego tech for ctfs i found the answer.

The key was XOR is a bitwise operator takes in a passcode of numbers and letters.

I found XOR in cyber chef and got the flag.

Flag = leveleffect{way_to_put_two_and_two_together}


