# Leaked and Loaded (100 Points) 🔐

## Challenge Description
A campaign manager, confident in their security knowledge, sent an encrypted password to a colleague. Our task is to decrypt and retrieve the passcode.

## Initial Analysis
We're presented with the following encoded string:
```text
ErcmE3yzD2KmQCWqDBbyhrqzh2qzEd1wfB59
```

## Solution Approach

### 1. Base64 Investigation
The string appears to be Base64 encoded. Looking for the Base64 pattern of `flag{}` which is `ZmxhZ3t9` helps identify potential flags.

### 2. ROT13 Analysis
```python
# Python code to perform ROT13
def rot13(text):
    result = ""
    for char in text:
        if char.isalpha():
            ascii_offset = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - ascii_offset + 13) % 26 + ascii_offset)
        else:
            result += char
    return result
```

### 3. Decryption Process
The decryption involved multiple stages:

| Stage | Operation | Result |
|-------|-----------|---------|
| 1 | Binary → Base64 | `ErcmE3yzD2KmQCWqDBbyhrqzh2qzEd1wfB59` |
| 2 | ROT13 | `RepzR3lmQ2XzDPJdQOoluedmu2dmRq1jsO59` |
| 3 | flag{} → Base64  | `ZmxhZ3t9` |
| 4 | ROT-N Variations | `ZmxhZ3tuY2FhLXRlYWwtcmluc2luZy1raW59`|
| 4 | Base64 → Text | `flag{ncaa-teal-rinsing-kin}`|


## Final Flag
```text
flag{ncaa-teal-rinsing-kin}
```

## Key Takeaways
- Multiple encoding layers were used
- Base64 encoding was the first layer
- ROT-N encryption provided additional security
- Pattern recognition was crucial for solving
- On generating ROT-N decryptions find the one that starts in the format of `ZmxhZ3t9`

## Tools Used
- Base64 decoder
- ROT13 cipher
- Custom ROT-N script
- Pattern matching tools

## Security Lessons
- Single-layer encoding is insufficient
- Known patterns (like flag format) can be exploited
- Complex encryption doesn't always mean better security

---
*Note: This challenge demonstrates the importance of proper encryption methods rather than relying on simple encoding schemes.*
