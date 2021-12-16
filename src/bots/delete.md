# Bot Delete

## Request
DELETE `/users/me/bots/{bot_id}`

## Response
### 204 No Content
Payload: none

### 403 Forbidden
Returned when the authorized user does not have permissions to delete this bot.

Payload: none

### 404 Not Found
Returned when any of the following are true:
* The user identified by `user_id` does not exist.
* The bot identified by `bot_id` does not exist.

Payload: JSON object describing the unknown item.