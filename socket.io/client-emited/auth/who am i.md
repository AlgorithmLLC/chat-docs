### who am i(ack)
Returns current user object

Error types:
  - `something went wrong`

Returns `user` object.
```javascript
result = {
  id: 1,
  first_name: "Иван",
  last_name: "Иванов",
  avatar: "270b67eb-923d-476b-8261-3",
  username: "10001",
  is_planned_password_change: false,
  is_planned_client_update: false,

  PublicKeys: [
    {
      id: 23,
      user_id: 1,
      name: "+lxTB5/JX/6MbWGZadUmxtCA=",
      is_default: true,
      created_at: "2014-09-02 15: 49: 03"
    }
  ],

  Domain: {
    id: 1,
    name: "Бирдэкс",
    url: "/",
    passphrase: "passphrase",
    config: {
      key_management_by_user: true,
      contactlist_management_by_user: true
    },
    is_base: true,
  }
}
```
