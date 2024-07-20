# MoTW

## Description

*NOTE* - The resources needed for this challenge are on the `Cyber Defense CTF Triage Workstation` VM on our [hosted platform](https://training.leveleffect.com/courses/f4a9466f-edb0-42ff-bb0e-a95af2b05de5).

Find out where the file `forest_stream.jpg` was downloaded from on the Triage Workstation and you'll have your flag!

# Method

This one was really quite easy.

First i just googled what a MOTW means which lead to understanding that it is called mark of the web. Which is a mark that is placed on files downloaded from the web that shows where the download took place.

Then i looked up how to identify this mark and found a powershell command to figure it out.

Get-Content -Path "yourfile.jpg" -Stream "Zone.Identifier"

This lead to the following link and the flag.

https://upload.wikimedia.org/wikipedia/commons/3/38/Teuchl_stream.jpg?flag=leveleffect%7Bgently_down_the_stream%7D

Flag = leveleffect{gently_down_the_stream}