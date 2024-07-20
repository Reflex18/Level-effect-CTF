# Ask and you shall recv 1

## Description

Connect to port `24194` on `0.cloud.chals.io` to get the flag.

# Method:

To obtain this flag i used ncat to connect to the port in the server.

The syntax was easy to find and was the following

ncat 0.cloud.chals.io 24194

Flag= leveleffect{socat_is_pretty_cool_too}

Since the flag name also implied using socat i tried that as well but had to search a bit more for the syntax

socat - TCP:0.cloud.chals.io:24194

to get the flag using socat