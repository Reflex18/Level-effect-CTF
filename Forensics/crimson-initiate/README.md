# Crimson initiate


## Description

*NOTE* - The resources needed for this challenge are on the `Cyber Defense CTF Triage Workstation` VM on our [hosted platform](https://training.leveleffect.com/courses/f4a9466f-edb0-42ff-bb0e-a95af2b05de5).

Let's dabble a bit on the offensive side. There is a user named `crimson` with admin privileges on the Triage Workstation. Use any method you prefer to get the user's password. The password is the flag.

You are able to download tools to the workstation if need be.

# method:

First lets run a command to find out if Crimson is really on the computer

I found the command for this was Net user

![Users crimson.png](Users%20crimson.png)

I also noticed that we have full admin rights on this account.

Therefore i searched up a way to obtain passwords of other accounts and where it was stored.

This lead me to the SAM file which is stored in: C:\Windows\System32\config

This file holds all of the passwords in hashes.

On looking up how to dump the file i found that there was an easy to use tool just for it called minikatz

The following article explained how to use the tool:

https://www.hackingarticles.in/password-dumping-cheatsheet-windows/

Effectively just run the exe in admin mode and then use the following three commands.

privilege::debug 

token::elevate 

lsadump::sam

![Crimson hash.png](Crimson%20hash.png)

Once I found the HASH NTLM i just went to crack station and pasted it in to find the password.

leveleffect{vermillion0727}