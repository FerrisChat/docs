# Create a Role

## Request
POST `/guilds/{guild_id}/roles`

### Payload
| Field | Type | Description | Default |
| ----- | ---- | ----------- | ------- |
| name | Option\<String> | name of this role | `new role` |
| color | Option\<i32> | color of this role | None |
| position | Option\<i16> | position of this role | 0 |
| permissions | Option\<Permissions> | permissions for this role | `Permissions::empty()` |

## Response
### 201 Created
Payload: role object describing the created role.