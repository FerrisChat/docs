# Bots

Bots are simply user objects with the bot flag set.

There are a few differences between them and normal users:
* Unlimited bots can be created, whereas only up to 40 users per residential IP,
and 4 per datacenter IP can be created
* Bots are linked to user accounts
* Bots cannot own bots
* Bot tokens are created by the owning user
* Bots can join unlimited servers
* Bots need to be invited by a guild member
* Bots cannot have relationships with users

Besides this, no other limits are applied, meaning a bot can access the entire API that a user can.

## Subsections
[Create](./create.md)

[Delete](./delete.md)

[Edit](./edit.md)