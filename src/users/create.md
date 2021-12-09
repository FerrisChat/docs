# Create a User

## Request
POST `/users`

### Payload
| Field    | Type   | Description                                                |
|----------|--------|------------------------------------------------------------|
| username | String | user name                                                  |
| email    | String | user email: note that no validation is done on this string |
| password | String | user password: no restrictions                             |

## Response
### 201 Created
Payload: user object describing the created user.

### 409 Conflict
Returned if any of the following are true:
* All available discriminators for this username are taken.
* A user with this email already exists.
