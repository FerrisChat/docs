# Create a Channel

In order to create a channel, you must send a POST request to `https://ferris.chat/api/v0/guilds/{guild_id}/channels`.

#### JSON Payload
| Field | Type | Description |
| ----- | ---- | ----------- |
| name | String | channel's name |

#### Example Response

```
200 OK

{
    "id": 954985616424781059018601791488,
    "name": "general",
    "guild_id": 953168419309560759306499915776
}
```