# Roles

A Role object is structured as follows:

| Name | Type | Description |
| ---- | ---- | ----------- |
| id | u128 | message id |
| guild_id | u128 | parent guild id |
| name | String | the name of this role |
| color | Option\<i32> | role color: integer between 0 and 16777215 |
| position | i16 | integer between 0 and 1023: the higher this number, the higher the role: if this number is the same as another, they will be sorted alphabetically |
| permissions | Permissions | the permissions this role has attached to it |
