# Token Details

Tokens are two pieces of base64 encoded data joined by a period.

For these examples we will use 
`MTA1NDc4Njk1NDUzODU2MjE4NzY3ODY5NDc2ODY0MA==.
BVwW6vC4gw-B6MVJGqqaaGWIw1saNFvEOH7cSLbcmJb53lv-wv4mUHKlpy_c0PiJeXbR57dqMy77iv8a5VZd1g==`
as an example token.

note: all Python examples were run with Python 3.8.10

## Part 1
`MTA1NDc4Njk1NDUzODU2MjE4NzY3ODY5NDc2ODY0MA==`

base64 encoded user ID
```python
import base64
token = "MTA1NDc4Njk1NDUzODU2MjE4NzY3ODY5NDc2ODY0MA==.BVwW6vC4gw-B6MVJGqqaaGWIw1saNFvEOH7cSLbcmJb53lv-wv4mUHKlpy_c0PiJeXbR57dqMy77iv8a5VZd1g=="
token = token.split(".")
print(int(base64.urlsafe_b64decode(token[0])))
```
```
1054786954538562187678694768640
```

### Part 2
`BVwW6vC4gw-B6MVJGqqaaGWIw1saNFvEOH7cSLbcmJb53lv-wv4mUHKlpy_c0PiJeXbR57dqMy77iv8a5VZd1g==`

random data
```python
import base64
token = "MTA1NDc4Njk1NDUzODU2MjE4NzY3ODY5NDc2ODY0MA==.BVwW6vC4gw-B6MVJGqqaaGWIw1saNFvEOH7cSLbcmJb53lv-wv4mUHKlpy_c0PiJeXbR57dqMy77iv8a5VZd1g=="
token = token.split(".")
print(base64.urlsafe_b64decode(token[1]))
```
```
b'\x05\\\x16\xea\xf0\xb8\x83\x0f\x81\xe8\xc5I\x1a\xaa\x9ahe\x88\xc3[\x1a4[\xc48~\xdcH\xb6\xdc\x98\x96\xf9\xde[\xfe\xc2\xfe&Pr\xa5\xa7/\xdc\xd0\xf8\x89yv\xd1\xe7\xb7j3.\xfb\x8a\xff\x1a\xe5V]\xd6'
```