# Save zig move zig

## Description

This is for the `Zig.exe` binary!

I am the name that called the zig mover.

Password to open archive: `infected`

*NOTE* - The resources needed for this challenge are on the `Cyber Defense CTF Triage Workstation` VM on our [hosted platform](https://training.leveleffect.com/courses/f4a9466f-edb0-42ff-bb0e-a95af2b05de5).

WARNING - This challenge involves malware. Do not run this on your personal machine. Use a VM in the Level Effect CTF course or your own. 

## Files

* [zig.zip](files/zig.zip)

# Method:

Based on the description of the challenge there might be a file of some type that was created from running the binary.

I used the windows search bar to look for any files that were added very recently.

This showed a file in the c\programs data which was a powershell file called movezig

There was nothing really of note here within the powershell file but the name of it matches the description.

![[Powershell output.png]]
At this point i noticed that a powershell script was being run on a timer.

So i took a look at the task scheduler to find if there was anything running it.

Sure enought there was a screensaver running this powershell script.

The flag then was = leveleffect{screensaver}

