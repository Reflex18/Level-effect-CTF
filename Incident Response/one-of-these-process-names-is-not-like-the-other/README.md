# One Of These Process Names Is Not Like The Other

## Description

This is for the `Zig.exe` binary!

I am the logger.

Password to open archive: `infected`

*NOTE* - The resources needed for this challenge are on the `Cyber Defense CTF Triage Workstation` VM on our [hosted platform](https://training.leveleffect.com/courses/f4a9466f-edb0-42ff-bb0e-a95af2b05de5).

WARNING - This challenge involves malware. Do not run this on your personal machine. Use a VM in the Level Effect CTF course or your own. 

## Files

* [zig.zip](files/zig.zip)

# Method:

I found this flag by accident really by just looking through task manager.

I was thinking about the concept of persistence and wondering if it added anything to start-up applications.

I noticed Rundlll32 that was just completely out of place when searching in the task manager for startup apps.

Sure enought that was the flag.

Flag = leveleffect{rundlll32.exe}