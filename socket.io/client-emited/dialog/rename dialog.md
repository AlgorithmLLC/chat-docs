### rename dialog(dialog, ack)
```javascript
dialog = {
  id: 443
  , "bodies": [
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
  ]
}
```
Saves renamed dialog.

Error types:
  - `something went wrong`

Returns saved `dialog object`.

### important notice
После успешного сохранения диалога необходимо отправить в этот диалоге сервисное сообщение
'Диалог переименован с “%старое название%” на “%новое название%”'
"message":
  {
    "dialog_id": %dialog_id%
    "type": "service.dialog.created"
  }
  "bodies":
  [
   …
  ]
