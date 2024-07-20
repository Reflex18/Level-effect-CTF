# Ask and you shall recv 2

## Description

Your goal is to SSH to `0.cloud.chals.io` over port `21986` using the private key provided for download. The passphrase is `cda-od`.

The username to connect with is the name of the operation led by law enforcement agencies in January 2021 that dealt a considerable blow to Emotet infrastructure.

**Note** - sharing private keys is always a bad idea - this is only for the purposes of the challenge.

## Files

* [p2.private.key](files/p2.private.key)

# Process:

First thing i did was to search up what the name of the operation led by the law enforcement agencies in January 2021. This led me to an article: https://ia.acs.org.au/article/2021/police-take-down-infamous-emotet-botnet.html

Within it the article stated that the name of the operation was Ladybird

Then using the syntax i tried to login to the ssh server

ssh -i p2.private.key Ladybird@0.cloud.chals.io -p 21986

![Too open.png](Too%20open.png)

To fix this issue i had to make the private key read only.

This required chmod 6000 "filename"

Then i tried again and found the flag

![Flag obtained.png](Flag%20obtained.png)
flag: leveleffect{private_keys_are_private_for_a_reason}