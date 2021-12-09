# Edit a Guild

## Request
PATCH `/guilds/{guild_id}`

### Payload
| Field  | Type            | Description                                               |
|--------|-----------------|-----------------------------------------------------------|
| name   | Option\<String> | guild name (must be between 1 and 100 Unicode codepoints) |

## Response
### 200 OK
Payload: new guild object

### 404 Not Found
Payload: description of this missing object
