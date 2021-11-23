# WebSocket Connection Flow

## Notes
* Do not send any sort of payload except for `Identify` until after you receive a `IdentifyAccepted`.
This includes `Ping` and `Pong`. Doing so will result in your connection being closed with code `2004`.

## Connection Flow
1) Start by making a GET request to `https://ferris.chat/api/v0/ws/info`. This returns a JSON payload.
**DO NOT HARDCODE THIS PAYLOAD RESPONSE**! It can and will change without warning.
```json
{
  "url":"wss://ws.api.ferris.chat"
}
```

2) Establish a WebSocket connection to the URL returned.
3) Once opened, send a [`Identify`](./events_inbound/identify.md) payload.
4) Wait for `IdentifyAccepted`
5) Once received, spawn a background task to send `Ping` payloads every 45 seconds.
6) When you wish to close the WebSocket, send a normal WebSocket close.
7) The server will respond normally and close the connection.