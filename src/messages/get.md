# Get a Message

## Request
GET `/channels/{channel_id}/messages/{message_id}`

## Response
### 200 OK
Payload: message object

Note that `nonce` will be None.

### 404 Not Found
Payload: details about the missing object.
