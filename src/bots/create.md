# Bot Create

## Request
POST `/users/me/bots`

### JSON Payload
| Field     | Type   | Description  |
|-----------|--------|--------------|
| username  | String | bot username |

## Response
### 201 Created
Payload: User object describing the new bot.
### 409 Conflict
Payload: JSON body. This code means all possible discriminators have been taken.