# WebSocket

The FerrisChat websocket is connectable via the url sent by `https://api.ferris.chat/v0/ws/info`.
It is important **NOT HARDCODE** this url, as it is subject to change.

The following events are currently sent:

| Name | When Fired | Format |
| ---- | ---------- | ------ |
| ChannelCreate | on channel create | `channel_{channel_id}_{guild_id}` |
| ChannelUpdate | on channel edit | `channel_{channel_id}_{guild_id}` |
| ChannelDelete | on channel delete | `channel_{channel_id}_{guild_id}` | 
| MessageCreate | on message send | `message_{channel_id}_{guild_id}` |
| MessageUpdate | on message edit | `message_{channel_id}_{guild_id}` |
| MessageDelete | on message delete | `message_{channel_id}_{guild_id}` |
| GuildCreate | on guild create | `guild_{guild_id}` |
| GuildUpdate | on guild edit | `guild_{guild_id}` |
| GuildDelete | on guild delete | `guild_{guild_id}` |
| MemberCreate | on member join | `member_{guild_id}` |
| MemberDelete | on member leave | `member_{guild_id}` |
| InviteCreate | on invite create | `invite_{guild_id}` |
| InviteUse | on invite use | `invite_{guild_id}` |
| InviteDelete | on invite delete | `invite_{guild_id}` |
