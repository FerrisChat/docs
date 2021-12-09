# Get Message History

## Request
GET `/channels/{channel_id}/messages`

### Query Parameters
| Field        | Type          | Description                                                               | Default   |
|--------------|---------------|---------------------------------------------------------------------------|-----------|
| limit        | Option\<i64>  | how many messages to fetch: None or 9,223,372,036,854,775,807 fetches all | None      |
| oldest_first | Option\<bool> | oldest messages first?                                                    | false     |
| offset       | Option\<i64>  | query cursor offset                                                       | 0         |

## Response
### 200 OK
Payload: `Vec<Message>`

Note that `nonce` will be None on all messages.

### 400 Bad Request
Returned if any of the following are true:
* limit is less than 0

### 404 Not Found
Payload: details about the missing object.
