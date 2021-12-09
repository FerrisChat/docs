# Edit a Role

## Request
PATCH `/guilds/{guild_id}/roles/{role_id}`

### Payload
| Field       | Type                 | Description               |
|-------------|----------------------|---------------------------|
| name        | Option\<String>      | name of this role         |
| color       | Option\<i32>         | color of this role        |
| position    | Option\<i16>         | position of this role     |
| permissions | Option\<Permissions> | permissions for this role |

## Response
### 200 OK
Payload: updated role object

### 404 Not Found
Returned if the requested role cannot be found.
