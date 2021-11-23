# Use an Invite

## Request
POST `/invites/{code}`

## Response
### 201 Created

### 400 Bad Request
Returned if any of the following are true:
* The code cannot be parsed as `String`.

### 403 Forbidden
Returned if any of the following are true:
* The user is not a member of the guild this invite is requested for.

### 404 Not Found
Returned if the invite is not found.

### 409 Conflict
Returned if the user has already joined this guild.

### 410 Gone
Returned if any of the following are true:
* The invite expired.
* The invite reached max uses.