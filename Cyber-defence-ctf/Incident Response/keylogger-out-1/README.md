# Keylogger Out #1

## Description

This is for the `Zig.exe` binary!

What was the file name for the first key logger output?

Password to open archive: `infected`

*NOTE* - The resources needed for this challenge are on the `Cyber Defense CTF Triage Workstation` VM on our [hosted platform](https://training.leveleffect.com/courses/f4a9466f-edb0-42ff-bb0e-a95af2b05de5).

WARNING - This challenge involves malware. Do not run this on your personal machine. Use a VM in the Level Effect CTF course or your own. 

## Files

* [zig.zip](files/zig.zip)

# Method:

![[Keylogger.png]]

The powershell file that was found in the other challenge of save zig move zig now comes into play.

The powershell file looks like it is uploading the base.out to a external website.

Checking if this was the keylogger and it is indeed.

Flag = leveleffect{base.out}