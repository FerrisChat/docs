# Identify

This should be the first thing you send to the WebSocket after connecting.

If successful, you will receive an [IdentifyAccepted](../events_outbound/identify_accepted.md) in response.
If there was an issue with authenticating you, the WebSocket connection will be closed.
[See details on closes here.](../close_codes.md)

| Field | Type | Default | Optional | Description |
| --- | --- | --- | --- | --- |
| token | String | None | false | The token from auth |
| intents | i64 | None | false | Gateway intents (ignored for now) |

```json
{
  "c": "Identify",
  "d": {
    "token": "",
    "intents": 0
  }
}
```