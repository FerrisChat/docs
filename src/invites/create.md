# Create a Channel

## Request
POST `/guilds/{guild_id}/invites`

### Payload
| Field | Type | Description |
| ----- | ---- | ----------- |
| max_age | Option\<i64> | after how many seconds should this invite expire? |
| max_uses | Option\<i16> | after how many uses should this invite expire? |

## Response
### 201 Created
Payload: channel object describing the new channel.

### 403 Forbidden
Returned if this invite is requested for a guild they are not a member of.
