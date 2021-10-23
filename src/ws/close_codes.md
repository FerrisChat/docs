# WebSocket Close Codes

Sometimes sh\*t happens. Connections get closed for random reasons. Here, most of the close reasons for the WebSocket are documented.

## Undocumented Codes

If a code is not documented here, but you receive it anyways, you can probably safely assume it's a bug (or perhaps a mistake in the docs).
Open a issue on the server repo.

## 1xxx Codes
These are usually lower-level transport errors, but some are user error.

| Code | Reason | Get new endpoint? | User Error? |
| ---- | ------ | ----------------- | ----------- |
| 1000 | Normal | N/A (conn closed normally) | No |
| 1001 | Endpoint going away | Yes | No |
| 1002 | Low-level protocol error | Yes | No |
| 1003 | Unsupported data type/info sent | Yes | Yes |
| 1006 | Abnormal closure (this is a bug) | Yes | No (bug) |
| 1007 | Invalid data (ie non-UTF8 in text msg) | Yes | Yes
| 1008 | Data violating policy | Yes | Yes |
| 1009 | Payload too large | Yes | Yes |
| 1011 | Internal server error | No | No |
| 1012 | Backend server restarting | No | No |
| 1013 | Server overloaded | No | No |
| 1014 | I/O error on underlying TCP socket | No | No |
| 1015 | TLS error | No | Maybe? |
| 1016 | Buffer capacity exhausted | No | Maybe? |
| 1017 | Invalid URL | No | Yes |
| 1018 | HTTP protocol error | No | Maybe? |
| 1019 | HTTP format error | No | Maybe? |

## 2xxx Codes
These are user errors.

| Code | Reason |
| ---- | ------ |
| 2001 | Invalid JSON |
| 2002 | More than 1 IDENTIFY payload sent |
| 2003 | Invalid token |
| 2004 | Data payload sent before IDENTIFY |

## 5xxx Codes
These are internal server errors. These are almost always the result of a bug. If you get one of these (except for 5000), expect more.

| Code | Reason |
| ---- | ------ |
| 5000 | Internal database error |
| 5001 | JSON serialization failure |
| 5002 | Redis pool not found |
| 5003 | Database pool not found |
| 5004 | User ID <-> Connection map not found |
| 5005 | Internal JSON representation decoding failure |

