### log out please(reason)
Emits when server restricts multi-device sessions and another device logs in.

Example: desktop client is logged in and user logs in with mobile device. Desktop client app recieves `log out please` event.

`reason` | Descrption
----- | ---
`null` | can be null
`"another device logged in"` |
