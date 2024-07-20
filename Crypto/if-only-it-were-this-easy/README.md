# If only it were this easy

## Description

Flag: `577ca2e5adb9dc46b44f668923055b238243f9b398c670584430e1e327141949ed345afce50fa4c9de130d3c331936cebd5104206a959daf74b9f15b68cfb193`

Key: `00112233445566778899aabbccddeeff00112233445566778899aabbccddeeff`

IV: `0102030405060708090a0b0c0d0e0f10`

## Method

For this challenge i searched up what kind of encryption used a string with a key and an iv.

This lead to understanding that it is an AES encryption, with this knowledge i used Cyberchef and put in the details then used the magic wand button to convert it from base 64 to get the flag.

Flag = leveleffect{keys_are_meant_to_be_kept}


![[AES%20Decrypt.png]]