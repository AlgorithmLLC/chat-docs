### update message(message, ack)
```javascript
message = {
  "id":6686,
  "bodies": [
    {
      "body":"waecuvhT2n7lT0Ofxv+wDtMJZg==",
      "nonce":"NJ8QcJrHYNYKFRdyT+gtc0arBsLpOFX7",
      "recipient_id":12,
      "key_id":305,
      "key_from_id":305
    },
    {
      "body":"28t9Y6t8zRwZA+FqXF9Na7nu+A==",
      "nonce":"Kf7XC+gYqXaOdYD4WKde7UX7s0lCYxTJ",
      "recipient_id":14,
      "key_id":333,
      "key_from_id":305
    }
  ],

  "toDelete":false // false - для изменения текста сообщения, true - чтобы пометить сообщение удаленным
}
```
Updates or deletes message.

Error types:
  - `something went wrong`

Returns updated `message object`.
