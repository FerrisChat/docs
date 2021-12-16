# Edit a User

## Request
PATCH `/users/{user_id}`

### Payload
| Field    | Type              | Description         |
|----------|-------------------|---------------------|
| username | Option\<String>   | new username        |
| email    | Option\<String>   | new email           |
| password | Option\<String>   | new password        |
| avatar   | Option\<String>   | URL to new avatar   |
| pronouns | Option\<Pronouns> | new set of pronouns |

## Response
### 200 OK
Payload: user object

Guilds are never returned.

### 403 Forbidden
Returned if the authenticated user is not the same as the one this edit targets.

### 404 Not Found
Returned if the requested user cannot be found.
