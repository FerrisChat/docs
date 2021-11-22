# Authentication

Bots and users have different authentication systems.

Bots need tokens created by the owning user: [find their details here](./bot_login.md)

Users just need an email and password to create a token: [find details here](./user_login.md)

Tokens should be attached to every request to the API after this as the `Authorization` header.
You do not need to prepend anything to the token.

Tokens are custom data we made just for FerrisChat: [find their details here](./tokens.md)