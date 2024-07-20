# Whose App Was It Anyway?

## Description

This is for the `Zig.exe` binary!

I ran the logger after I mislead you from the first console screen.

Password to open archive: `infected`

*NOTE* - The resources needed for this challenge are on the `Cyber Defense CTF Triage Workstation` VM on our [hosted platform](https://training.leveleffect.com/courses/f4a9466f-edb0-42ff-bb0e-a95af2b05de5).

WARNING - This challenge involves malware. Do not run this on your personal machine. Use a VM in the Level Effect CTF course or your own. 

## Files

* [zig.zip](files/zig.zip)

# Method:

To figure out this one i used the autoruns program from the sysinternals suite.

I pressed the hide windows entities so that only non windows programs show up and had the category set to everything.

A particular program appeared called myApp that was in the image path of Rundlll32.exe which was found to be created as apart of the zigs.exe.

I tested it and it was the flag.

Flag = leveleffect{MyApp.exe}

![[Myapp zig.png]]