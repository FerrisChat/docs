# WebSocket Close Codes

Sometimes sh\*t happens. Connections get closed for random reasons. Here, most of the close reasons for the WebSocket are documented.

## Undocumented Codes

If a code is not documented here, but you recieve it anyways, you can probably safely assume it's a bug (or perhaps a mistake in the docs).
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

## 5xxx Codes
These are internal server errors. These are almost always the result of a bug, or perhaps a simple database reconnect that came at a bad time.

| Code | Reason |
| ---- | ------ |
| 5000 | Internal database error |
| 5001 | JSON serialization failure |
