# Users

A User object is structured as follows:

| Name          | Type              | Description                                              |
|---------------|-------------------|----------------------------------------------------------|
| id            | u128              | user id                                                  |
| name          | String            | user name                                                |
| avatar        | Option\<String>   | user avatar URL                                          |
| guilds        | Vec\<Guild>       | list of all the guilds a user is in                      |
| flags         | UserFlags         | user flags                                               |
| discriminator | i16               | user discriminator: between 1 and 9999                   |
| pronouns      | Option\<Pronouns> | user pronouns: see [Pronouns](./pronouns.md) for details |
