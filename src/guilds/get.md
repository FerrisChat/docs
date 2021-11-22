# Get a Guild

## Request
GET `/guilds/{guild_id}`

### Query Parameters
| Field | Type | Description | Required | Default |
| ----- | ---- | ----------- | -------- | ------- |
| members | boolean | return a list of members? | false | false |
| channels | boolean | return a list of channels? | false | true |

## Response
### 200 OK
Payload: requested guild object

### 404 Not Found
Payload: description of this missing object
