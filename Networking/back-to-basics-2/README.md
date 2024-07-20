# Back to basics 2

## Description

Which nameserver is the SOA (Start of Authority) for the [leveleffect.com](https://www.leveleffect.com/) domain?

# Method:

I used dig to output information about the site

Then found the SOA in that information

ns-1327.awsdns-37.org.

Then converted that to the flag

leveleffect{ns-1327.awsdns-37.org}

job done

