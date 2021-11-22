# Fetch a Channel

## Request
GET `/channels/{channel_id}/`

## Response
### 200 OK
Payload: channel object describing the new channel.

### 404 Not Found
Payload: JSON object describing the unknown channel.