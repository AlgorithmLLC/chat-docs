### auth by token(credentials, ack)
```javascript
credentials = {
  userId: 15
  , token: '5afe96fa-dc35-40a7-b7be-8c322fb20501'
}
```
Performs authentication by `token` from `auth by credentials`.

Error types:
  - `wrong data provided` — bad userId or token or they're not specified
  - `wrong token, use credentials` — token not found or it's expired

You must fallback to username/password authentication on error.

Returns `token` and `userId` on success.
```javascript
result = {
  userId: 15
  token: '5afe96fa-dc35-40a7-b7be-8c322fb20501'
}
```
