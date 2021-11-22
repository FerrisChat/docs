# Bot Authentication
## Notes
* The user who owns the bot must run this.
* Fetching a new token invalidates previous ones. This will not change.

## Request
POST `/users/{user_id}/bots/{bot_id}/auth`

### Payload
None

## Example Response
### 200 OK
Payload: JSON object with one field named `token`.
### 403 Forbidden
Returned if you are not the owner of this bot. 

Payload: none
