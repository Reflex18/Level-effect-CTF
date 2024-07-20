When you engaged with the virulent Sprawl2.exe program, who were you this time?

**[i] README** - You can access the challenge binary from the `Cyber Defense CTF - 2nd Phase Triage Workstation` VM on our [hosted platform](https://training.leveleffect.com/courses/2a4dccb7-3d5b-4312-816e-ef3728d25b67). You can also [download](https://github.com/Level-Effect/CyberDefenseCTF-Public/raw/main/Challenges/2024/The%20Sprawl2/theSprawl2.zip) the binary from our GitHub.

**[!] WARNING** - This challenge has malware-like behavior involved. DO NOT run this on your personal machine. Use a VM in the Level Effect CTF course or your own.

Unlock Hint for 50 points

Unlock Hint for 50 points

Submit

[Powered by CTFd](https://ctfd.io/)

# Method:

![[Sprawl 2 program.png]]


The sprawl 2 exe when launched displays the following command prompt asking for a login.

I have looked up the wiki for the shadowrun series based on the previous spawl challenges and entered in the following names.

Kitsune: Since this character shapeshifts into a fox and can cast powerball

Along with the following five characters that are all her enemies within the book.

- **Coyote**
- **Hector**
- **Shango**
- **Sister Sin**
- **The Ghost**

None of these so far have been correct.

Using strings on the exe managed to final the following information.

![[Strings spawl part 1.png]]

Strings provided a few flags for it:

leveleffect{YOU-ARE-THE-FOX}