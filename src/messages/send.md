# Send a Message

In order to send a message, you must send a POST request to `https://ferris.chat/api/v0/channels/{channel_id}/messages`.

#### JSON Payload
| Field | Type | Description |
| ----- | ---- | ----------- |
| content | String | message content (must be at or below 10240 characters) |

#### Example Response

```
201 CREATED

{
    "id": 962733210640370448862516609024,
    "content": "FerrisChat FTW",
    "channel_id": 954985616424781059018601791488,
    "author_id": 1
}
```