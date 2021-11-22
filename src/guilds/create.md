# Create a Guild

## Request
POST `/guilds`

### Payload
| Field | Type | Description |
| ----- | ---- | ----------- |
| name | String | guild name (must be between 1 and 100 Unicode codepoints) |

## Response
### 201 Created
Payload: guild object describing the created guild.
