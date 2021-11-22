# Delete a Message

## Request
DELETE `/channels/{channel_id}/messages/{message_id}`

## Response
### 200 OK
Payload: message object describing the updated message.

### 400 Bad Request
Returned if any of the following are true:
* Message content length is > 10,240 Unicode codepoints

### 404 Not Found
Payload: details about the missing object.
