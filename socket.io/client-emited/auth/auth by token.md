### auth by token(credentials, ack)
```javascript
credentials = {
  userId: 15
  , token: '5afe96fa-dc35-40a7-b7be-8c322fb20501'
  , isLightweight: false
}
```
Performs authentication by `token` gathered from successful `auth by credentials` request.

##### isLightweight
This parameter is optional and is `false` by default. This parameter narrows down client recieved events list and its contents to reduce client-server network activity and traffic.

`isLightweight: true` sockets will be subscribed to and recieve only this events:
  - log out please
  - subscribe please
  - messages (event will be shrink and will not contain body and attachments)

#### Error types:
  - `wrong data provided` — bad userId or token or they're not specified
  - `wrong token, use credentials` — token not found or it's expired

You must fallback to username/password authentication on error.

#### Returns
`token` and `userId` on success. Next `auth by token` calls must be done with last returned token.
```javascript
result = {
  userId: 15
  token: '5afe96fa-aaaa-40a7-bbbb-8c322fb20501'
}
```
