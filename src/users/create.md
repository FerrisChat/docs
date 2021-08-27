# Create a User

In order to create a user, you must send a POST request to `https://ferris.chat/api/v0/users`.

#### JSON Payload
| Field | Type | Description |
| ----- | ---- | ----------- |
| username | String | user's preferred name |
| email | String | a user's email |
| password | String | a users password |

#### Example Response

```
201 CREATED

{
    "id": 1,
    "name": "hydrostaticcog",
    "guilds": null,
    "flags": 0
}
```