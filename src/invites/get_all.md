# Get Guild Invite

## Request

GET `/guilds/{guild_id}/invites`

## Response
### 200 OK
Payload: `Vec<Invite>`

### 403 Forbidden
Returned if the user is not a member of this guild.
