# Bot Edit

## Request
PATCH `/users/me/bots/{bot_id}`

### JSON Payload
| Field    | Type            | Description   |
|----------|-----------------|---------------|
| username | Option\<String> | bot username  |

## Response
### 200 OK
Payload: User object describing the updated bot.

### 403 Forbidden
Returned when the authorized user does not have permissions to edit this bot.

Payload: none

### 404 Not Found
Returned when any of the following are true:
* The user identified by `user_id` does not exist.
* The bot identified by `bot_id` does not exist.

Payload: JSON object describing the unknown item.