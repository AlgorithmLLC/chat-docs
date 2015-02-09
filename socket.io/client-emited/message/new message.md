### new message(message, ack)
```javascript
message = {
  "message": {
    "dialog_id":"434"
  }

  // Зашифрованное тело сообщения, в том числе для отправителя
  "bodies": [
    {
      "nonce":"lE9DrayttnvLzgQyHHYjtx2UiUh0AbAw",
      "recipient_id":12,
      "key_id":305,
      "key_from_id":305,
      "body":"WXpviVsU7spyCn4Q8ZyETXFfHA=="
    },
    {
      "nonce":"XhakTAhyV0knGw+R/DOKlKHKtrlq8h3E",
      "recipient_id":14,
      "key_id":333,
      "key_from_id":305,
      "body":"/X5CtECjTsJi7KZelNvEBQRyJQ=="
    }
  ],

  // Вложения, если есть
  "attachments": [
    {
      "unique":"7f0a62be-ddb7-4cc5-97f4-51e5d8daf08d",
      "size":523764,
      "bodies":
      [
        {
          "name":"yhHFQTVZzZ79501cMMp9nKOGHzhBKhBtWmuMyT0=",
          "nonce":"XKXQQNotR+y4TuVr6V9MzSbZuxXwz5yK",
          "crypto":"F7ZRCT3W84sDAD2wCKOR05vIGCdtJhQ9BGfei3hayG9Yvurf91NvVD9/",
          "recipient_id":12,
          "key_id":305,
          "key_from_id":305
        },
        {
          "name":"sjOrEJoAU98/EZSGPx6q+Z+n6djdZxVNANp2SeY=",
          "nonce":"EDENc6HXI/SZGZdpwC8TvKAdLgnh2WTq",
          "crypto":"eb2lEP6aPkb8+r26iz7jVKfp7sfxaxEdXtYkC6MtHBKuJigPnOGlcLXb",
          "recipient_id":14,
          "key_id":333,
          "key_from_id":305
        }
      ]
    }
  ]
}

```
Saves new message.

Error types:
  - `something went wrong`

Returns saved `message object`.
