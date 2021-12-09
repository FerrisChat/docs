# Invites

A Invite object is structured as follows:

| Name       | Type         | Description                                                         |
|------------|--------------|---------------------------------------------------------------------|
| code       | String       | the invite's unique code                                            |
| owner_id   | u128         | the owner of this invite                                            |
| guild_id   | u128         | the guild this invite belongs to                                    |
| created_at | i64          | the time this invite was created in seconds since the Ferris Epoch  |
| uses       | i32          | number of times this invite was used                                |
| max_uses   | Option\<i32> | the maximum number of times this invite can be used before expiring |
| max_age    | Option\<i64> | how many seconds after creation this invite will expire             |