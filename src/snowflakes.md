# Snowflake IDs

Snowflakes are 128 bit unsigned integers.

```text
00000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^Group 1 ^^^^^^^^^^^^^^^^Group 3 ^^^^^^^^^^^^^^^^ Group 5
Group 0                                                         ^^^^^^^^ Group 2        ^^^^^^^^ Group 4        ^^^^^^^^^^^^^^^^
```
## Group 0
64 bits

`snowflake >> 64`

Time this snowflake was generated, in milliseconds since the Ferris Epoch (01/01/2022 00:00:00.000000 -0000)

```python
# coding=utf-8
import datetime

snowflake = 426882856118070100650360832
# the Ferris Epoch is 1 trillion, 640 billion, 995 million, and 200 thousand milliseconds after the Unix Epoch
ferris_epoch_offset = 1_640_995_200_000

snowflake_timestamp_offset_ms = snowflake >> 64
print(snowflake_timestamp_offset_ms)
# 23141366

snowflake_timestamp_ms = snowflake_timestamp_offset_ms + ferris_epoch_offset
print(snowflake_timestamp_ms)
# 1641018341366
snowflake_timestamp = snowflake_timestamp_ms / 1000
print(snowflake_timestamp)
# 1641018341.366
snowflake_datetime = datetime.datetime.utcfromtimestamp(snowflake_timestamp)
print(snowflake_datetime)
# 2022-01-01 06:25:41.366000
```

## Group 1
8 bits

`snowflake >> 56 & 0b11111111`

The type of snowflake.

### Snowflake Types
* Guild: 0
* User: 1
* Channel: 2
* Message: 3
* Role: 4
* InternalUse: 5
* Unknown: !0 == 255

```python
# coding=utf-8
import enum
snowflake = 426882856118070100650360832

class ModelType(enum.IntEnum):
    Guild = 0
    User = 1
    Channel = 2
    Message = 3
    Role = 4
    InternalUse = 5
    Unknown = 2 ** 8 - 1

model_type = snowflake >> 56 & 0b11111111
print(model_type)
# 0

model_type_enum = ModelType(model_type)
print(model_type_enum)
# ModelType.Guild
```

## Group 2
16 bits

`snowflake >> 40 & 0b1111111111111111`

Internal node counter. This is not of much use.

```python
# coding=utf-8
snowflake = 426882856118070100650360832

internal_counter = snowflake >> 40 & 0b1111111111111111
print(internal_counter)
# 24
```

## Group 3

8 bits

`snowflake >> 32 & 0b11111111`

The API version this snowflake was made on.

```python
# coding=utf-8
snowflake = 426882856118070100650360832

api_version = snowflake >> 32 & 0b11111111
print(api_version)
# 0
```

## Group 4

16 bits

`snowflake >> 16 & 0b1111111111111111`

The internal node ID of this snowflake. Nodes do not have a consistent ID.
This is again not of much use.

```python
# coding=utf-8
snowflake = 426882856118070100650360832

internal_id = snowflake >> 16 & 0b1111111111111111
print(internal_id)
# 11132
```

## Group 5

16 bits

`snowflake & 0b1111111111111111`

Unset bits. 
These were used to identify early users, who could set these bits if they wanted.

```python
# coding=utf-8
snowflake = 426882856118070100650360832

unset = snowflake & 0b1111111111111111
print(unset)
# 0
```
