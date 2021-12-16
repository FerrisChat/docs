# Create a Channel

## Request
POST `/guilds/{guild_id}/channels`

### Payload
| Field  | Type   | Description    |
|--------|--------|----------------|
| name   | String | channel's name |

## Response
### 201 Created
Payload: channel object describing the new channel.
