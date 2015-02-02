### new dialog(dialog, ack)
```javascript
dialog = {
  "bodies": [
    {
      "nonce":"JEjfSlc0tJ"
      ,"recipient_id":"14"
      ,"key_id":336
      ,"key_from_id":211
      ,"name":"u9RlNfl=="
    },
    {
      "nonce":"1nogNkxCKh"
      ,"recipient_id":"12"
      ,"key_id":211
      ,"key_from_id":211
      ,"name":"ctebdww=="
    }
  ],
  "recipients":["14","12"],
  "dialog":{"group_id": "12"} // Если этот диалог принадлежит группе, иначе {}
}
```
Saves new dialog.

Error types:
  - `something went wrong`

Returns saved `dialog object`.

### important notice
После успешного создания диалога необходимо отправить в этот диалоге сервисное сообщение
'Создан новый диалог.'
"message":
  {
    "dialog_id": %dialog_id%
    "type": "service.dialog.created"
  }
  "bodies":
  [
   …
  ]
