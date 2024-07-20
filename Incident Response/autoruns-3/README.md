# Autoruns 3

## Description

Attackers compromised this Windows host and riddled it with persistence mechanisms in a see-what-sticks effort to maintain a foothold on the system. Can you find the third persistence mechanism?

*NOTE* - The resources needed for this challenge are on the `Cyber Defense CTF - Autoruns Challenges` VM on our [hosted platform](https://training.leveleffect.com/courses/f4a9466f-edb0-42ff-bb0e-a95af2b05de5).

# Method:

This happened to be the first one i managed to find.

I first checked the task scheduler to see if anything weird was placed here.

I noticed that the disk cleaner was running a strange looking script that was obfuscated

This lead me to checking the registry key for the property 

The value name of the key then decoded into the flag.

Also of note the value data is base64 encoded for the command "whoami"

![Autoruns 3.png](Autoruns%203.png)

Flag = leveleffect{its_becoming_self_aware}