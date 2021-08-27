# Get a Message

In order to get a message, you must send a GET request to `https://ferris.chat/api/v0/channels/{channel_id}/messages/{message_id}`.

#### Example Response

```
200 OK

{
    "id": 962733210640370448862516609024,
    "content": "FerrisChat FTW",
    "channel_id": 954985616424781059018601791488,
    "author_id": 1
}
```