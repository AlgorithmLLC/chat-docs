### subscribe please(reason)
Emits when server wants client app to authenticate or reauthenticate.

Brings `reason` with value of:
  - `null`
    not expected, but must work
  - `"token expired"`
    emited when authentication expired
