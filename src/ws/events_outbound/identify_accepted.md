# IdentifyAccepted

After successfully sending an [Identify](../events_inbound/identify.md),
you will either get a closed connection or this event.

Upon receipt of this event, you are free to send anything to the server.

| Field | Type | Description |
| --- | --- | --- |
| user | User | The now-authenticated user. |

Guilds are populated, and members are populated on the guilds.

```json
{
  "c": "IdentifyAccepted",
  "d": {
    "user": {
      "id": 1088869216590563422205939810304,
      "id_string": "1088869216590563422205939810304",
      "name": "0/0",
      "avatar": null,
      "guilds":[
        {
          "id": 1088707735803565215231395758080,
          "id_string": "1088707735803565215231395758080",
          "owner_id": 1088706545416795447876311842816,
          "owner_id_string": "1088706545416795447876311842816",
          "name": "FerrisChat",
          "channels": [
            {
              "id": 1088708020492310624377028214784,
              "id_string": "1088708020492310624377028214784",
              "guild_id": 1088707735803565215231395758080,
              "guild_id_string": "1088707735803565215231395758080",
              "name": "general"
            }
          ],
          "members":[
            {
              "user_id": 1088706545416795447876311842816,
              "user_id_string": "1088706545416795447876311842816",
              "user": {
                "id": 1088706545416795447876311842816,
                "id_string": "1088706545416795447876311842816",
                "name": "hydrostaticcog",
                "avatar": null,
                "guilds": null,
                "flags": 3072,
                "discriminator": 1
              },
              "guild_id": 1088707735803565215231395758080,
              "guild_id_string": "1088707735803565215231395758080",
              "guild": null
            }
          ],
          "roles": null,
          "flags": 0
        }
      ],
      "flags": 3584,
      "discriminator": 1
    }
  }
}
```