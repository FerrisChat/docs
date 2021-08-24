# Create a Guild

In order to create a guild. you must send a POST request to `https://ferris.chat/api/v0/users` with the payload:

#### JSON Payload
| Field | Type | Description |
| ----- | ---- | ----------- |
| name | String | guild name (must be between 1 and 100 Unicode codepoints) |

#### Example Response

```
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