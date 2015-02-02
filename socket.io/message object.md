### message object
```javascript
message = {
  "id":6674,
  "dialog_id":423, // Диалог, в котором это сообщение отправлено
  "edited_at":null, // Дата изменения текста сообщения, если сообщение было отредактировано
  "type":"message.default", // Message type, see below
  "created_by":12,
  "created_at":"2015-01-15 14:51:54",
  "updated_by":12,
  "updated_at":"2015-01-15 14:51:54",

  // Основная информация о создателе сообщения
  "Creator": {
    "id":12,
    "username":"10002",
    "domain_id":1
  },

  // Зашифрованный текст сообщения
  "Body": {
    "id":5529,
    "body":"smSfyeu8LLqsbzj13rFRuA==",
    "nonce":"je6nazCv+pEjePLlnHvqDS0++sNmwnMb",
    "key_id":305,
    "key_from_id":305,
    "read_date":"2015-01-15 14:51:54", // Дата, когда сообщение было прочитано
    "is_received":false, // Пока не используется
    "props":null, // игнорировать
    "message_id":6674, // игнорировать
    "recipient_id":12, // игнорировать
    "created_at":"2015-01-15 14:51:54",
    "updated_at":"2015-01-15 14:51:54"
  }

  // Вложения в сообщение
  "Attachments": [
    {
    "id":2559,
    "unique":"31b43023-333c-459f-a804-dd07bd28f72b",
    "size":528610,
    "message_id":6674,
    "Message":false,
    "created_at":"2015-01-15 14:51:54",
    "updated_at":"2015-01-15 14:51:54",

    // Зашифрованный контейнер с именем файла и ключом для его расшифровки
    "Body": {
      "id":508,
      "name":"lcJvXbJcQuFeDd9WPYpQ/4yYF4yJx/aM2C64nzw=",
      "attachment_id":2559,
      "recipient_id":12,
      "crypto":"8ngvmz9UIwJeo4kP+7oxWrTWEJOly/LchiLq3Xlcv5oVv4",
      "nonce":"ogWG+pCTRH1LQ1IlkOUAdFWKyidlduYH",
      "key_id":305,
      "key_from_id":305,
      "created_at":"2015-01-15 14:51:54",
      "updated_at":"2015-01-15 14:51:54"
    }
    }
  ],
}
```

Message types:
  - user typed messages:
      - `message.default`
      - `message.deleted`
      - `message.updated`
  - service messages:
      + calls-related:
          - `service.call.audio.missed`
          - `service.call.audio.finished`
          - `service.call.audio.noanswer`
          - `service.call.video.missed`
          - `service.call.video.finished`
          - `service.call.video.noanswer`
      * groups and dialogs manipulations:
          - `service.group.created`
          - `service.group.user.invited`
          - `service.group.user.kicked`
          - `service.group.renamed`
          - `service.dialog.renamed`
