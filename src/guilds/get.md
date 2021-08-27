# Get a Guild

In order to get a guild, you must send a GET request to `https://ferris.chat/api/v0/guilds/{guild_id}`.

#### Query Params
| Field | Type | Description | Required | Default |
| ----- | ---- | ----------- | -------- | ------- |
| members | boolean | decides whether a list of members is returned | false | false |
| channels | boolean | decides whether a list of channels is returned | false | true |

#### Example Response

```
200 OK

{
    "id": 953168419309560759306499915776,
    "owner_id": 1,
    "name": "FerrisChat",
    "channels": [
        {
            "id": 954985616424781059018601791488,
            "name": "general",
            "guild_id": 953168419309560759306499915776
        }
    ],
    "members": null
}
```