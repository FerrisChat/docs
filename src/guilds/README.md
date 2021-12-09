# Guilds

A Guild object is structured as follows:

| Name     | Type          | Description                         |
|----------|---------------|-------------------------------------|
| id       | u128          | guild id                            |
| owner_id | u128          | guild owner's id                    |
| name     | String        | name of the guild                   |
| channels | Vec\<Channel> | list of all the channels in a guild |
| members  | Vec\<Member>  | list of all the members in a guild  |
