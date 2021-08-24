# FerrisChat User

### Create a User

In order to create a user, you must send a POST request to `https://ferris.chat/api/v0/users` with the payload:
```
{
    "username": username,
    "email": email,
    "password": password
}
```

You will receive a User object back that contains the ID. Do not lose that ID, as you will need it to fetch the user later.