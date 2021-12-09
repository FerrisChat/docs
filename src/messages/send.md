# Send a Message

## Request
POST `/channels/{channel_id}/messages`

### Payload
| Field   | Type            | Description                                      |
|---------|-----------------|--------------------------------------------------|
| content | String          | message content (1 to 10,240 Unicode codepoints) |
| nonce   | Option\<String> | message nonce                                    |

## Response
### 201 Created
Payload: message object describing the created message.

### 400 Bad Request
Returned if any of the following are true:
* Message content length is > 10,240 Unicode codepoints

### 404 Not Found
Payload: details about the missing object.
