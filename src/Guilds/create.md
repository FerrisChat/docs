# Create a Guild

In order to create a guild. you must send a POST request to `https://ferris.chat/api/v0/users` with the payload:

#### JSON Payload
| Field | Type | Description |
| ----- | ---- | ----------- |
| name | String | guild name (must be between 1 and 100 Unicode codepoints) |

You will receive a Guild object back that contains the ID. Do not lose that ID, as you will need it to fetch the guild.