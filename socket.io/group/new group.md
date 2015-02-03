### new group(group, ack)
```javascript
group = {
  "bodies": [
    {
      "nonce":"+MpRANHLYJG9MBnoVYhY0NYRrvKEJHC7",
      "recipient_id":14,
      "key_id":330,
      "key_from_id":211,
      "name":"8z+rr0EVtQhmuaeDmug8ZNONo9IbbfFCWSESTEEEx2lI8pgC"
    },
    {
      "nonce":"KPAsSawjvzCo5pZG+9nu/ykBLXFTTpOY",
      "recipient_id":12,
      "key_id":211,
      "key_from_id":211,
      "name":"COe3RSQ0qcZG7eHPCgBfhZqYMqmI5W0GqaszbLEfFaduTRtK"
    }
    , 
    ... 
    ,
    {}
  ],
  "recipients":[14,12], // участники группы
  "admin_id":12, // создатель и в дальнейшем администратор группы
  "avatar":"311d6400-14ae-4247-af7a-4269bbc64a00" // аватар группы
}
```
Saves new group.

Error types:
  - `something went wrong`

Returns saved `group object`.

### important notice

Создание группы состоит из трех последовательных операций
__Создание группы -> Создание диалога -> Отправка сервисного сообщения__

1. После успешного создания групппы необходимо добавить в группу диалог с названием 'Основной'
2. После успешного добавления диалога необходимо отправить в этот диалог сервисное сообщение.

Текст сообщения для отправителя __'Создана новая группа. Этот диалог создан автоматически.'__

Текст сообщения для каждого из получателей __'Вы добавлены в новую группу. Это самое начало переписки.'__

```
"message":
  {
    "dialog_id": %dialog_id%
    "type": "service.group.created"
  }
  "bodies":
  [
   …
  ]
```
