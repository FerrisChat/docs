# Login

By logging in, you generate a token use for authentication. You MUST add this token to pretty much all of your requests.

Send a POST request to `https://api.ferris.chat/v0/auth`.

#### Request Headers
```
Email: email
Password: password
```

#### Example Response
```
{
    "token": "token"
}
```

Reauthenticating will invalidate previous tokens.
