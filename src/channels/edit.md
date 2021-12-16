# Update a Channel

## Request
PATCH `/channels/{channel_id}`

### Payload
| Field | Type            | Description    |
|-------|-----------------|----------------|
| name  | Option\<String> | channel's name |

## Response
### 200 OK
Payload: channel object describing the new channel.

### 404 Not Found
Payload: JSON object describing the unknown channel.
