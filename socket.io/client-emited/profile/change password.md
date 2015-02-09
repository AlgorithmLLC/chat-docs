### change password(password, ack)
```javascript
password = {
  current: "123"
  , new: "456"
  , newAgain: "456"
}
```
Changes password.

Error types:
  - `wrong data provided`
  - `new password must match verify`
  - `new password must not match old`
  - `wrong password`

This frame's ack returns no data.
