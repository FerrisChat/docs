# Edit a Message

## Request
PATCH `/channels/{channel_id}/messages/{message_id}`

### Payload
| Field   | Type            | Description                                      |
|---------|-----------------|--------------------------------------------------|
| content | String          | message content (1 to 10,240 Unicode codepoints) |
| nonce   | Option\<String> | message nonce                                    |

## Response
### 200 OK
Payload: message object describing the updated message.

### 400 Bad Request
Returned if any of the following are true:
* Message content length is > 10,240 Unicode codepoints

### 403 Forbidden
Returned if the authenticated user is not the user who owns the message

### 404 Not Found
Payload: details about the missing object.
