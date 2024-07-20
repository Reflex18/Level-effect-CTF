# What you say!?

## Description

This is for the `Zig.exe` binary!

This response would have bought you a little more time!

Password to open archive: `infected`

*NOTE* - The resources needed for this challenge are on the `Cyber Defense CTF Triage Workstation` VM on our [hosted platform](https://training.leveleffect.com/courses/f4a9466f-edb0-42ff-bb0e-a95af2b05de5).

WARNING - This challenge involves malware. Do not run this on your personal machine. Use a VM in the Level Effect CTF course or your own. 


## Files

* [zig.zip](files/zig.zip)

# Method:

Starting the challenge now. lets see what the zip holds

This exe asks a response from the person.

Reponse 1 restarts your computer in 10 seconds
If you respond 2 then it restarts the computer in 20 seconds
3 is right away
4 is also right away

since the challenge is incident response, what tool can i use to see the ICO?

After much testing with different methods to see what the binary does while it is running i have found that the flag is just the full response for number 2.

Flag = leveleffect{What you say!?}

Yes i was very dumb founded when i found it out.



