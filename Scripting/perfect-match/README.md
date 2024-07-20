# Perfect match

## Description

Regex - love it or hate it, it's an invaluable skill to have as a defender.

The goal of this challenge is to extract all IPv4 addresses from the contents of the file `input.txt` . A starter script has been provided below and by download. All you need to do is insert a regex pattern to finish the job. You can submit your code in the code submission box.

Note: If you write your own script, you must read in the data from `input.txt` specifically as shown in the example.

Starter script:
```python
import re

PATTERN = re.compile(r'YOUR PATTERN HERE')

def extract_ips(data):
    ips = PATTERN.findall(data)

    unique_ips = []
    [unique_ips.append(str(ip)) for ip in ips if ip not in unique_ips]

    return unique_ips

def main():
    with open("input.txt") as f:
        data = f.read()
        extracted_ips = extract_ips(data)

    for ip in extracted_ips:
        print(ip)

main()
```

# Method: 

Code submission box:

```
import re

PATTERN = re.compile(r'\b(?:25[0-5]|2[0-4]\d|1\d{2}|[1-9]?\d)(?:\.(?:25[0-5]|2[0-4]\d|1\d{2}|[1-9]?\d)){3}\b')

def extract_ips(data):
    ips = PATTERN.findall(data)

    unique_ips = []
    [unique_ips.append(str(ip)) for ip in ips if ip not in unique_ips]

    return unique_ips

def main():
    with open("input.txt") as f:
        data = f.read()
        extracted_ips = extract_ips(data)

    for ip in extracted_ips:
        print(ip)

main()
```
Correct code

I used chat gpt to ask for the regex value and then asked it again to remove any ip addresses that are clearly not ip addresses since it was incorrect the first time.

## Files

* [extract.py](files/extract.py)

* [input.txt](files/input.txt)

