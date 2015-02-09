### auth by credentials(credentials, ack)
```javascript
credentials = {
  username: '10003'
  , password: '10003'
}
```
Performs authentication by `username` and `password`.

Error types:
  - `wrong data provided` — bad username or password or they're not specified
  - `wrong password` — username not found or password mismatch

Returns `token` and `userId` on success.
```javascript
result = {
  userId: 15
  token: '5afe96fa-dc35-40a7-b7be-8c322fb20501'
}
```

You must not save `username` and `password`.
You should save token and use it lately to perform auth on reconnect.
