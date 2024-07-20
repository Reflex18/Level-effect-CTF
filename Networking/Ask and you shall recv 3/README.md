# Ask and you shall recv 3

## Description

This time, the flag is hosted on a webserver running *internally* at `0.cloud.chals.io` on port `8888`. SSH is exposed on port `27141`. The private key for user `tunneler` is provided for download and the passphrase is `cda-od`.

Can you figure out how to get to the flag?

**Note** - sharing private keys is always a bad idea - this is only for the purposes of the challenge.

## Files

* [p3.private.key](files/p3.private.key)

# Method:

Much like the ask and recv 2 i first made sure to use chmod 600 "privatekeyname" to mark the key as read only permissions.

Then i attempted to ssh in using the following syntax to see what happens

ssh -i p3.private.key tunneler@0.cloud.chals.io -p 27141

![No%20quite.png](Not%20quite.png)

I got the following information from it which prompted some googling.

After some information searching i learnt about the concept of an SSH tunnel.

This was what the syntax was

ssh -i /path/to/private_key -L 8888:localhost:8888 -p 27141 tunneler@0.cloud.chals.io

Then after tunneling into it I needed to quickly put in the following url.

http://localhost:8888

leveleffect{attack_from_within}

![Tunne%20made.png](Tunnel%20made.png)