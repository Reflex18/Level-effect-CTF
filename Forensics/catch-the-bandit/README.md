# Catch the bandit

## Description

Can you catch the bandit and recover the flag?

WARNING - The binary in this challenge is benign but we advise to run it on a VM. Do not run this on your personal machine. Use a VM in the Level Effect CTF course or your own. 

## Files

* [bandit.exe](files/bandit.exe)

# Method:

First i tried to run the bandit.exe in my linux vm and found that i could not open it.

On using file command on it i found that it required ms windows.

`bandit.exe: PE32 executable (console) Intel 80386, for MS Windows, 16 sections'

So i searched up how to run it in linux and found i needed a compatibility layer called wine.

so i installed it via `sudo apt install wine

Was unable to launch the exe in my vm so i started up the VM from level effect.

First I am just going to run it and see what happens, not advisable sure but it is in a VM.

Note this ended up bricking the vm's gui and forced me to load a snapshot...
Dont do this but if you do anything do it in a vm with a backup. :D

Attempt two:

So next thing i did was trying to figure out what the exe did by checking the windows event logs and searching for the flag of leveleffect.

This proved fruitless so i rethought what i needed to do and recalled that it ran a command line for a split second before going away.

So i used the following command to try and figure out what was output to maybe provide some more information about this exe.

bandit.exe > output.txt

This instead provided the exact flag i needed...

Wow, that was easier then i thought

Flag = leveleffect{b4nd17_c4ugh7}

