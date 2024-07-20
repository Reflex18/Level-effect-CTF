# Pasta filiformis

## Description

On to the second course, pasta filiformis with a tangy reduction. Save room for dessert!

# Method

This is a challenge that provided a zip file

The code within it was base64 encoded that converted into morse code using cyber chef.

Then the code converted into words that spelt out ZERO and ONE over and over when i converted it using cyber chef.

There were also some zere and ro in it which made it a bit tricky to understand.

I used a find and replace tool to make zere into 0 since it appears to be a spelling mistake while the ro i turned into space bars.

I converted this via an online binary to text translator with ascii/utf-8 which got the following output.

Site: https://www.rapidtables.com/convert/number/binary-to-ascii.html

OVXGK3TVNZXW63TMMN5TO4JUG42V6NC7MJ4TC3DIL53DGNBXNM2DCML5

Then put it back into cyber chef to obtain the following output

unenunoonlc{7q475_4_by1lh_v347k411}

This looked like a flag but it wasnt in the right format since i need leveleffect at the front

Therefore i inferred that the letters were shifted since that was the case with a prior challenge.

So i looked up a ceaser cipher converter online since i knew what the shift was already by counting the change from u to l. The shift for this was 17 letters.

Flag = leveleffect{7h475_4_sp1cy_m347b411}

Is the final flag and a bit more involved one this time but also used alot of tactics that was done in prior challenges.
